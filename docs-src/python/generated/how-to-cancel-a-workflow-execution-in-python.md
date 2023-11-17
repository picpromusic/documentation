---
id: how-to-cancel-a-workflow-execution-in-python
title: How to Cancel a Workflow Execution in Python
sidebar_label: Cancel a Workflow Execution
description: Cancel a Workflow Execution with Retry Policies.
tags:
- workflow execution
- retry policy
- python sdk
- code sample
---

<!-- DO NOT EDIT THIS FILE DIRECTLY.
THIS FILE IS GENERATED from https://github.com/temporalio/documentation-samples-python/blob/replay-tests/workflow_failures/workflow_dacx.py. -->

<div class="copycode-notice-container"><div class="copycode-notice"><img data-style="copycode-icon" src="/icons/copycode.png" alt="Copy code icon" /> Sample application code information <img id="i-459237d1-7c6c-4ef5-99a4-cefff89610bc" data-event="clickable-copycode-info" data-style="chevron-icon" src="/icons/chevron.png" alt="Chevron icon" /></div><div id="copycode-info-459237d1-7c6c-4ef5-99a4-cefff89610bc" class="copycode-info">The following code sample comes from a working and tested sample application. The code sample might be abridged within the guide to highlight key aspects. Visit the source repository to <a href="https://github.com/temporalio/documentation-samples-python/blob/replay-tests/workflow_failures/workflow_dacx.py">view the source code</a> in the context of the rest of the application code.</div></div>

```python
from temporalio.common import RetryPolicy
```