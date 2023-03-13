---
id: how-to-connect-to-a-development-cluster-in-go
title: How to connect to a Temporal dev Cluster in Go
sidebar_label: Connect to a dev Cluster
description: Use the Dial() method on the Temporal Client and omit setting any client options. If there is a local dev Cluster running, the Client will connect to it.
---

Use the [`Dial()`](https://pkg.go.dev/go.temporal.io/sdk/client#Dial) API available in the [`go.temporal.io/sdk/client`](https://pkg.go.dev/go.temporal.io/sdk/client) package to create a new [`Client`](https://pkg.go.dev/go.temporal.io/sdk/client#Client).

If you don't provide [`HostPort`](https://pkg.go.dev/go.temporal.io/sdk/internal#ClientOptions), the Client defaults the address and port number to `127.0.0.1:7233`, which are the ports of the development Cluster.

If you don't set a custom Namespace name in the Namespace field, the client connects to the default Namespace.

<a class="dacx-source-link" href="https://github.com/temporalio/documentation-samples-go/blob/main/yourapp/gateway/main_dacx.go">View source code</a>

```go
package main

import (
	"context"
	"encoding/json"
	"log"
	"net/http"

	"documentation-samples-go/yourapp"

	"go.temporal.io/sdk/client"
)


func main() {
	// Create a Temporal Client to communicate with the Temporal Cluster.
	// A Temporal Client is a heavyweight object that should be created just once per process.
	temporalClient, err := client.Dial(client.Options{
		HostPort: client.DefaultHostPort,
	})
	if err != nil {
		log.Fatalln("Unable to create Temporal Client", err)
	}
	defer temporalClient.Close()
// ...
	// Set the options for the Workflow Execution.
	// A Task Queue must be specified.
	// A custom Workflow Id is highly recommended.
	workflowOptions := client.StartWorkflowOptions{
		ID:        "your-workflow-id",
		TaskQueue: "your-custom-task-queue-name",
	}
	// Use an object as your Workflow Function parameter.
	// Objects enable your Function signature to remain compatible if fields change.
	workflowParams := yourapp.YourWorkflowParam{
		WorkflowParamX: "Hello World!",
		WorkflowParamY: 999,
	}
	// Make the call to the Temporal Cluster to start the Workflow Execution.
	workflowExecution, err := temporalClient.ExecuteWorkflow(
		context.Background(),
		workflowOptions,
		yourapp.YourWorkflowDefinition,
		workflowParams,
	)
	if err != nil {
		log.Fatalln("Unable to execute the Workflow", err)
	}
// ...
}
```