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

If we get rid of all the features I find unpleasant, above, what are we left with? No mocks, no fake data, short, simple, repeatable, independent tests. Unit tests of stateless utility functions are a prime example of this.

```js
test("Two plus two is four", () => {
  expect(plus(2, 2)).toBe(4);
});
```

If I were writing library of functions to do arithmetic I could surround my code with a battery of such tests and maintain them for years without having to tax my lazy brain. Bliss.

### Be an enabler

We've established what we think makes a maintainable set of tests. Now we need to figure out how to write code that enables these features.

One way is to continue being lazy. Don't think about what your code should look like. Write the tests you want to write, and then make code that passes them. This method is called Test-driven development (TDD). One of its advantages is that it forces you to design a testable boundary for your code. If you're doing TDD, and you find yourself getting frustrated before you've even made your first assertion, you may wish to re-think the unit of code you're designing.

## Boundaries
