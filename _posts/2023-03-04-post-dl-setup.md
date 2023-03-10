---
title: "My at-home deep learning setup - March 2023"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - hardware
  - deep-learning
hidden: false
published: true
---

Machine learning, and deep learning in particular, can impose some hefty computational requirements which can be a barrier for getting started. There are a lot of great cloud-based workarounds, but maybe you just wanna hear those fans spin up under your own desk, ya know?

I have had success running DL models locally on a PC I built primarily for gaming with no hardware changes. I still play games occasionally, but now my GPU mostly spends it's days computing convolutions.



# Hardware

I built my current pc in 2014, and it is starting to show its age a bit. I upgraded the GPU in 2018-ish. I also did the RAM and added a second SSD at some point.

CPU: Intel 4690K @ 3.5 GHz  
GPU: NVIDIA GeFORCE GTX 1080 (8 GB)  
Memory: 16 GB DDR3  
Storage: 128 GB SSD boot drive, 1 TB SSD (both SATA)  
Motherboard: Gigabyte z97x  

For deep learning projects, the key features here are the amount of VRAM on my GPU (8 GB), which sets the maximum size of models I can train, as well as having a decent amount of CPU RAM, and SSD storage space for storing datasets.

When I rebuild, I'd go for a much bigger card, if only [3090Ti prices](https://pcpartpicker.com/products/video-card/#c=520) would ever come down :(



# OS

For DL projects, I run Ubuntu 22.04, which I dual-boot alongside windows 10. 

I set this up by downloading the [ubuntu iso](https://releases.ubuntu.com/jammy/) and flashing it to a thumb drive using [Balena Etcher](https://www.balena.io/etcher). This was my first time installing a linux distribution, and it went pretty smoothly. 

The only key set up step was to **check a box for "download 3rd party drivers during installation"**. This got me the nvidia graphics drivers on install, avoiding any [big headaches](https://askubuntu.com/questions/1129516/black-screen-at-boot-after-nvidia-driver-installation-on-ubuntu-18-04-2-lts).

Pictured: a happy nvidia-smi directly after ubuntu install, complete with CUDA!
![Image: a happy nvidia-smi directly after ubuntu install](/assets/images/nvidia-smi.png)



# Software

I mostly write python which I manage using [Anaconda](https://www.anaconda.com/products/distribution).

The deep learning framework I have most experience with is [pytorch](https://pytorch.org/). I currently use pytorch1.13.

For other packages/versions, check the [requirements.txt](https://github.com/dthuff/pet-vae/blob/master/requirements.txt) in one of my project repos.

Specific to medical imaging, I like using [3DSlicer](https://www.slicer.org/) for viewing and editing 3D images.