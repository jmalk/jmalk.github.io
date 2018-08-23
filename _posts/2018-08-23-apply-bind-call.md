---
layout: post
title: "Apply, Bind and Call in JavaScript"
date: 2018-08-23
---

## bind

Bind is a method on JavaScript functions. It allows you to do at least two things.

First, it lets you set what `this` will be for the function. Whatever object you choose, that's what the function will understand `this` to be.

Second, you can use bind to pre-set some arguments for the function.

Let's say you have some generic add function, and you want to make a more specific version. The more specific version only takes one number and always adds five to it.

```
function add (a, b) {
  return a + b;
}

console.log(add(4, 3));
// Prints 7 to the console, I hope...

const addFive = add.bind(null, 5);

console.log(addFive(4));
// Prints 9 to the console.
```

So addFive is effectively the same as defining a function like

```
function addFive (number) {
  return 5 + number;
}
```
