---
layout: post
title: "Creating Testable Boundaries"
date: 2021-01-26
---

## Testable

When we write code, we want to write tests for it, so that we don't have to keep checking the same things manually as our program becomes more complex. But we are lazy, and we want those tests to be easy to write. If those tests are in an area of the codebase that's likely to change, we also want the tests to be easy to maintain.

Let's start from this side - instead of asking what makes source code easy to test, let's ask what makes tests (relatively) pleasant to write and maintain. We can probably work this out by thinking about the worst tests we've ever touched.

### My least favourite tests

- Dozens of mocks and stubs.
- Lots of fake data.
- Long.
- Too much nesting, complex loops.
- Inconsistent results when running. (AKA "flaky" tests.)
- Dependencies between tests. e.g. If you swap the order of two tests, they no longer work.

### My favourite tests

## Boundaries
