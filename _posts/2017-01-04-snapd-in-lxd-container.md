---
layout: post
title:  "在lxd container裡用snap"
date:   2017-01-04 09:20:28 +0800
---

怎麼測試是方便,當然是跑lxd container.
然而snappy 16因為架構改變, 基本上snap格式由原本相容於deb/click轉變為squashfs.
這樣一個缺點就是在container裡面要支援比較麻煩, Ubuntu也是在去年11月左右才算把這個問題弄好.
我還蠻期待在container裡面run all snap的, 應該不清楚還有什麼還沒處理好的.

https://bugs.launchpad.net/snappy/+bug/1611078

詳見: https://www.stgraber.org/2016/12/07/running-snaps-in-lxd-containers/


Ubuntu 16.04(backported)/ 16.10 host
Stock Ubuntu kernel (4.8.0)
Stock LXD (2.4.1 or higher)
Ubuntu 16.10 container with “squashfuse” manually installed in it

on xenial

 host $ lxc attach ubuntu:16.04 snap-in-lxd
 host $ lxc exec snap-in-lxd
 snap-in-lxd # apt update
 snap-in-lxd # apt upgrade
 snap-in-lxd # apt install squashfuse
 snap-in-lxd # snap install hello
 ...
