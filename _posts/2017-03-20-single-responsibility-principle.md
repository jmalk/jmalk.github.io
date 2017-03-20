---
layout: post
title: "Single Responibility Principle"
date: 2017-03-20
---

Let's start with a seemingly tangential question:

## What is "good quality" code?

When we say code is good, what qualities does it have that bad code doesn't? I thought of a few, and my tutor helped fill out the list of examples.

* Readable. I can understand what each bit of it intends to do.
* Consistent. There is one way of doing something throughout.
* Extensible. I can add to it relatively quickly and easily.
* Testable. I can change it with reasonable confidence that I haven't broken something else.
* Low WTFs/min. This is a "metric" I first saw in Clean Code. How many times does someone exclaim WTF when first reading the code.
* Execution efficiency. Is it fast at what it does?
* Low number of bugs, low rate of additional bugs.
* Release tempo. FOLLOW-UP: Why is this a sign of good code?

## Single Responsibility Principle makes code better

My tutor is so confident in the power of Single Responsibility Principle (SRP) that they asserted "SRP can make all of these qualities easier to achieve, and so make your code better".

The SRP can be applied at many scales, from the responsibility of a single variable, to that of a large system. In between these extremes lie functions, which should have a focussed responsibility, though this does not need to be done dogmatically to the point of every function being only one line of code.

## How to draw your lines

Given the assertion that code divided into chunks with well-defined responsibilities is easier to extend, test, release and maintain, how should we divide up our code? You can do this any which way you choose. So how do we make good choices?

A prevailing opinion in this space is, if the behaviour of some part of your system is likely to change regularly, bring this code together and isolate it from the rest of the app. Then you can change it without having to touch many parts of the codebase. This allows you to test that behaviour with fewer worries about regressions introduced elsewhere in the app.

This allows you to build and release software *faster*, and your stakeholders will thank you. Well they might not thank you, but at least they won't get angry at you for going slowly.

---

[Why write modular code?](https://twitter.com/b0rk/status/771044569341394944)
