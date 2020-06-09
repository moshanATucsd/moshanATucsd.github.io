---
layout: post
title: How to make a word cloud from pdfs
categories:
tags:
---

I would like to make a word cloud from the papers I have published, so here it is!

![word cloud](/images/posts/wordCloud.png)

The simple word cloud shows that my research is focused on semantic understanding of images, by extracting features to recover motion and reconstruct objects. Moreover, I have probably used the word 'method' too much in my papers...

The colab code can be found [here](https://gist.github.com/moshanATucsd/3551e51c39ca35cef394618b0e7b2fc3).

Later I found another cool [word cloud generator](https://github.com/amueller/word_cloud), we need to convert pdf to text first using `pdftotext doc.pdf`, and the code is

<script src="https://gist.github.com/moshanATucsd/adc1218fb84039ca5f8e87f06d04fa54.js"></script>
