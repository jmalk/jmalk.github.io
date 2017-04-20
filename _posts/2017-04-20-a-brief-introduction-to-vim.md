---
layout: post
title: "A Brief Introduction to Vim"
date: 2017-04-20
---

## What I find it useful for

Really fast text editing.

## What I don't find it useful for (yet)

Navigating big projects is so much easier with Atom. Getting a "feel" for a new large codebase.

## NeoVim

Modern defaults, e.g. mouse is enabled.

## The absolute basics

Open a file from the command line with `vim filename`. Vim starts in Normal mode. In "Normal" mode, keypresses don't generally insert text.

Press `i` (or `a` or `o` or `O` or...) to enter Insert mode. Now letters will appear under the cursor! Like a real text editor!!

After you've finished editing text, `Esc` gets you back to Normal mode. Type `:wq` to [w]rite and [q]uit.

## Teach yourself

Run `vimtutor`.

## Movements and text objects

I <3 Vim because it uses individual keypresses rather than chords, allowing you to type commands with a natural action.

I <3 it even more because you can combine commands and movements in a way that becomes intuitive. Trying some sequence of keypresses, thinking to myself "I wonder if this will work?" and seeing that it does indeed do what I expected it to, brings a little bit of joy to an otherwise mundane task.

### Moving the cursor to where you want it

There are lots and lots of ways to move the cursor around with the keyboard. Typical motions:

Move one character down: j, up: k, left: h, right: l.

Move one word forward: w, back: b.

Move to the next occurence of the letter `y` on this line: fy. (Mnemonic "find y".)

Move to the previous occurence of the letter `y` on this line: Fy (shift often reverses the effect of commands, but not always).

Move to start of line: 0

Move to end of line: $

### Manipulating text

If you want to delete some text, you press `d`. But how much text? However much you want! Combine `d` with a motion from the previous section (Moving the cursor to where you want it) and Vim will delete the text between your current cursor position and wherever that move takes you. e.g. `dw` will delete until the next word.

* c = change (delete then enter insert mode so you can type something new)
* d = delete (functions a bit like Cut though, as it puts it in the copy register)
* y = yank (copy)
* x = delete character

Now we can have fun combining verb-like commands with noun-like text objects. 

* cw = change to end of word
* daw = delete word cursor is in
* y3w = yank three words
* dd = ?
* cc = ?

## I done goofed

To undo the last change you made in insert mode, hit `u` in normal mode. That's `u` for undo. To redo what you undid, it's <C-r>.

## DRY text editing

I'm not going to try and cover all of Vim in this because I don't know it all, and even if I did, it'd bore you to tears.

But I am going to mention the dot command. Typing a `.` in Normal mode repeats whatever you just did. So let's say you make a shopping list, like apples, bananas, bread, eggs, and milk, then think "actually I prefer chocolate...

```
apples, bananas, bread, eggs, milk
```

You use `cw` to change-word apples to chocolate.

```
chocolate, bananas, bread, eggs, milk
```

Then hit `w` a couple of times, or `fb` to move the cursor onto the 'b' of 'bananas'. At this point, hit `.` and it will repeat the last change. (Change word to chocolate).

```
chocolate, chocolate, chocolate, chocolate, chocolate
```

:wq
