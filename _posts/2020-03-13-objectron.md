---
layout: post
title: 3D object detection on a mobile phone 
categories:
tags:
---

Recently I read about [this article](https://ai.googleblog.com/2020/03/real-time-3d-object-detection-on-mobile.html) and was amazed by the app's ability to detect 3D objects in real time, so I decided to give it a try. 

I followed the [docker installation](https://github.com/google/mediapipe/blob/master/mediapipe/docs/install.md#installing-using-docker) to build the mediapipe first, then build the [objectdetection3d](https://github.com/google/mediapipe/tree/master/mediapipe/examples/android/src/java/com/google/mediapipe/apps/objectdetection3d) for android. This is the shoe detection only. After the docker build finish I need to copy the apk from the docker to my local machine via `docker cp mediapipe:mediapipe/bazel-bin/mediapipe/examples/android/src/java/com/google/mediapipe/apps/objectdetection3d/objectdetection3d.apk /dest_dir`

The chair version is provided at [objectron](https://github.com/google/mediapipe/blob/master/mediapipe/docs/objectron_mobile_gpu.md). 

I only have a MBP so I spent some time figuring out how to transfer the apk to android phone. Eventually I downloaded the google drive on the phone and install the apk from there. Here are the results, the poses are very accurate, but the speed is very slow. I used redmi note 7 and the video mode turned into picture mode...

![img](/images/posts/shoe1.jpg)
![img](/images/posts/shoe2.jpg)
![img](/images/posts/shoe3.jpg)

The [paper](https://arxiv.org/abs/2003.03522) is also released, and it says the EPnP details are in the supplementary. I am curious about how the authors define the 3D points of each object in the EPnP. 





