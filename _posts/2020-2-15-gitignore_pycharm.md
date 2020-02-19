---
layout: post
title: Ignore cached files in Pycharm
categories:
tags:
---

Here's the gitignore to remove config files in Pycharm

```
.idea/
/**/__pycache__/
/**/.DS_Store
```

If we forget to add gitignore at first, we could remove all the tracked but unwanted files by [this answer](https://stackoverflow.com/questions/1274057/how-to-make-git-forget-about-a-file-that-was-tracked-but-is-now-in-gitignore)

```
git rm -r --cached .
git add .
git commit -am "Remove ignored files"
```
