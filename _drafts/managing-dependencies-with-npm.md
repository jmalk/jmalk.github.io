---
layout: post
title: "Managing Dependencies with npm"
date: 2019-03-22
---

## SemVer
A brief intro: breaking, adding, fixing.

## Repeatable builds!
Why do we care?
* Can rebuild an old version of the system if there’s a bug in a running instance of it we need to diagnose.
* We all build the project separately but we want to get the same result! We also want the same result as what goes into production.

## NPM package version notation
What do tilde and carats mean? Without them you stay on exact versions.

## Nested dependencies
Your package.json doesn’t specify the version of your dependency’s dependency. If an update is released to it, your project might take that change. Maybe you won’t realise and maybe it’ll break your project.

## Lock files and shrink wrap
A package-lock.json specifies what code to install for every dependency, including children, grandchildren, etc.

Shrink wrap matters to package authors. We aren’t releasing our code to npm so we don’t have to care.

## npm install
What do I get? What changes if I run it again?

## npm ci
As above, what do I get? What if I run it again? What if it’s out of step with package.json? What’s the difference between this and install?

npm ci will not write to your package or package lock files.

It is stricter than npm install.