---
layout: post
title: How to set system python
categories:
tags:
---

Recently I tried [bonnetal](https://github.com/PRBonn/bonnetal/tree/master/deploy/src/segmentation) and accidentally changed my system python by
```
sudo update-alternatives --install /usr/bin/python python /usr/bin/python2.7 1
```

In fact, we could use `sudo update-alternatives --config python` to select python versions. The default one for ubuntu 1604 is python 2.7, which is also used by ROS. Only when we enter conda, the python version changes to python 3.6.

Also note that in `~\.bashrc`, we need the path in following order
```
# for ros
source /opt/ros/kinetic/setup.bash
#this should be after ros
export PATH="$PATH:/home/erl/anaconda3/bin"
```
