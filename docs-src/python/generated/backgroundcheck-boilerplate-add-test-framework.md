---
id: backgroundcheck-boilerplate-add-test-framework
title: Add a testing framework
sidebar_label: Test framework
description: How to add a testing framework to your Temporal Application.
tags:
- testing
- developer guide
- test framework
- python sdk
---

<!-- DO NOT EDIT THIS FILE DIRECTLY.
THIS FILE IS GENERATED from https://github.com/temporalio/documentation-samples-python/blob/replay-tests/backgroundcheck_boilerplate/tests/workflow_dacx_test.py. -->

Each Temporal SDK has a testing suite that can be used in conjunction with a typical language specific testing framework.
In the Temporal Python SDK, the testing package (https://python.temporal.io/temporalio.testing.html) provides a test environment in which the Workflow and Activity code may be run for test purposes.