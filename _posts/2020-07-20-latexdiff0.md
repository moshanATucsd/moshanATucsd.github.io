---
layout: post
title: How to use latexdiff
categories:
tags:
---

When we want to show the difference in the latex files, we can use `latex diff` as follows
```
brew install latexdiff
latexdiff --flatten old/main.tex new/main.tex > diff/main.tex
```
where `flatten` means to combine the tex files in all subfolders. 

Then we can upload the `diff/main.tex` to overleaf to download the pdf that highlights the changes.
