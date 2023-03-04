---
title: "My at-home Deep Learning setup"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
hidden: false
published: true
---

# Hardware

I built my current pc in 2014, and it's starting to show it's age a bit. GPU was upgraded in 2018-ish. I also did the RAM and added a second SSD at some point.

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

The only key set up step was to check a box for "download 3rd party drivers during installation". This got me the nvidia graphics drivers on install, avoiding any [big headaches](https://askubuntu.com/questions/1129516/black-screen-at-boot-after-nvidia-driver-installation-on-ubuntu-18-04-2-lts)

Image: a happy nvidia-smi directly after ubuntu install
![Image: a happy nvidia-smi directly after ubuntu install](/assets/images/nvidia-smi.png)

# Software

I mostly write python which I manage using [Anaconda](https://www.anaconda.com/products/distribution).

The deep learning framework I have most experience with is [pytorch](https://pytorch.org/).

Specific to medical imaging, I like using [3DSlicer](https://www.slicer.org/) for viewing and editing 3D images.