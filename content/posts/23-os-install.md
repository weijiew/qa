---
title: '浅谈操作系统加载流程（装系统）'
date: 2021-03-05
published: false
slug: 23-os-install
tags: ['Linux','操作系统']
cover_image: "./images/p23.jpg"
canonical_url: false
description: ''
---

# 1. 前言

最近装了一个 Arch ，号称最难装的系统，装完之后发现其实没多难。

而操作系统已经安装过数次了，但是一直对于原理不是很理解，正好借助这篇文章来理清思路。

Arch 的包管理工具是我用过所有里面最好的，几乎没有遇到任何依赖问题。其次滚动更新能时刻保证软件版本处于最新版。例如 Python 直接默认内置 3.9 。缺点是可能会把系统滚挂，这个问题可以通过备份，快照来弥补。

# 2. 操作系统加载流程

CPU 加电后会首先启动 BIOS ， BIOS 是一段在出厂的时候就写死的程序，也就是只读。接下来就是 BIOS 将操作系统加载到内存中。某种意义上而言操作系统就是字节数组，是一个程序。

接下来读取的是存储设备的第一个扇区，该扇区大小为 512 MB，前 448 字节存放引导程序，后 64 字节存放分区表。引导程序将操作系统加载到内存中，

> 还没想清楚，等我想清楚再写，不喜欢边学边写。