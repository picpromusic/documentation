---
id: backgroundcheck-boilerplate-add-test-framework-details
title: Add a testing framework details
sidebar_label: Test framework details
description: How to add a testing framework to your Temporal Application.
tags:
- testing
- developer guide
- test framework
- go sdk
---

<!-- DO NOT EDIT THIS FILE DIRECTLY.
THIS FILE IS GENERATED from https://github.com/temporalio/documentation-samples-python/blob/replay-tests/backgroundcheck_boilerplate/tests/workflow_dacx_test.py. -->

The `BackgroundCheck` Workflow code checks the following conditions:

1. It receives a social security number and a unique ID as input parameters.
2. It starts a new Activity `ssn_trace_activity` with the input SSN.
3. It waits for the Activity to complete and returns the result.
4. If the Activity returns "pass", it logs a message indicating that the background check passed.
5. If the Activity returns "fail", it raises an exception indicating that the background check failed.

We can also perform a Workflow Replay test, and we'll provide detailed coverage of this topic in another section.