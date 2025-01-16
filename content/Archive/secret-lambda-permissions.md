---
title: "Secret Lambda Permissions"
date: "2016-12-02"
updated: 2023-03-26
categories:
  - "words"
---

[This](https://docs.aws.amazon.com/lambda/latest/dg/access-control-resource-based.html) is the culmination of half a days work trying to figure out why my Lambda function didn’t fire:

> The console doesn’t support directly modifying permissions in a function policy. You must use either the AWS CLI or the AWS SDKs.

In other words: it is a secret setting that we hide from you. Just in case you’re trying to use a versioned lambda function or a function alias.
