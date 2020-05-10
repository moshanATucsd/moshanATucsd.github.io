---
layout: post
title: Ubuntu 18.04 installation
categories:
tags:
---

## Prepare the USB drive

- [prepare the USB stick on Mac](https://ubuntu.com/tutorials/tutorial-create-a-usb-stick-on-macos#1-overview)
- [prepare the USB stick on Ubuntu](http://ubuntuhandbook.org/index.php/2018/10/create-live-usb-ubuntu-18-04/), basically download the release, use `Start Disk Creator` in ubuntu to create the installation stick.

## Install

- press `F12` when starting the computer and select `install ubuntu` then press `e` in the grub menu
- find `quite splash`, delete `---` after that, and add `nomodeset`, press `F10`
- we can use the default partition to install ubuntu, no need to partition on our own

## Restart

- after installation, we need to restart, keep the USB stick plugged in and press `F12` when restarting
- in grub menu, press `e` at the `ubuntu` option and find `quite splash`, add `nomodeset` after it, press `F10`
- after seeing the desktop, open a terminal and enter `sudo gedit /etc/default/grub`, change `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"` to `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash nomodeset"`, then `sudo update-grub`

## NVIDIA

- at this time after restart the resolution is not correct, we need to install nvidia driver via [this post](https://askubuntu.com/questions/1118621/cannot-install-nvidia-390-driver-ubuntu-18-04), [this post](https://www.mvps.net/docs/install-nvidia-drivers-ubuntu-18-04-lts-bionic-beaver-linux/)
- after installing the drive, we can also install CUDA 
