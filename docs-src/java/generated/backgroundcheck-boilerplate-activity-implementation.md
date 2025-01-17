---
id: backgroundcheck-boilerplate-activity-implementation
title: Boilerplate Activity Implementation
sidebar_label: Activity code
description: In the Temporal Java SDK, an Activity Definition is an interface and its implementation.
tags:
- java sdk
- developer guide
- activity
- code sample
---

<!-- DO NOT EDIT THIS FILE DIRECTLY.
THIS FILE IS GENERATED from https://github.com/temporalio/documentation-samples-java/blob/durable-execution/backgroundcheck/src/main/java/backgroundcheckboilerplate/BackgroundCheckBoilerplateActivitiesImpl.java. -->

Now that you've defined your Activity Interface you can define its implementation.

<div class="copycode-notice-container"><div class="copycode-notice"><img data-style="copycode-icon" src="/icons/copycode.png" alt="Copy code icon" /> Sample application code information <img id="i-d883a0f8-8624-400b-813e-6269c3a7ed9b" data-event="clickable-copycode-info" data-style="chevron-icon" src="/icons/chevron.png" alt="Chevron icon" /></div><div id="copycode-info-d883a0f8-8624-400b-813e-6269c3a7ed9b" class="copycode-info">The following code sample comes from a working and tested sample application. The code sample might be abridged within the guide to highlight key aspects. Visit the source repository to <a href="https://github.com/temporalio/documentation-samples-java/blob/durable-execution/backgroundcheck/src/main/java/backgroundcheckboilerplate/BackgroundCheckBoilerplateActivitiesImpl.java">view the source code</a> in the context of the rest of the application code.</div></div>

```java
public class BackgroundCheckBoilerplateActivitiesImpl implements BackgroundCheckBoilerplateActivities{

  @Override
  public String ssnTraceActivity(String socialSecurityNumber){
    
    // This is where a call to another service would be made to perform the trace
    // We are simulating that the service that does SSNTrace executed successfully
    // with a passing value being returned

    String result = "pass";
    return result;
  }

}
```
