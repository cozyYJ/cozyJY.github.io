---
layout: post
title: Github page is not updating a new post
subtitle: Life is pain you know...
categories: Git, Github
tags: [Git, Github]
published: true
---

## Problem

After writing _(JAVA) Can't input using nextLine()_, this new buddy was well generated in my local server (localhost:4000), unfortunately not in the real github page... :(

It took around 2hrs to fix this ordeal!

### Solution

- Check that the form of the file name (**YEAR-MONTH-DAY-title.md**) is written correctly.
- Try adding **published: true** to the option of a page section (section containing layout, title, categories, etc.).
- Try adding **future: true** to _\_config.yml_
- Try editing _index.html_ by adding some tirivial changes like one space.

## Source

[devyuseon, githubblog-post-not-shown](https://devyuseon.github.io/github%20blog/githubblog-post-not-shown/)
