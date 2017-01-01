---
layout: post
title:  "威力強大的 classic confinement"
date:   2017-01-01 15:20:28 +0800
---

在snapcraft 2.24的[Release Note](<https://github.com/snapcore/snapcraft/releases>)中,
有兩個非常重要的功能, classic confinement 跟 top level commands(alias).

classic confinement會讓snap裡面的環境跟實際系統的環境一樣.
這雖然違背snap一開始設計snap被封裝在特定的環境比如有特定HOME/TMP,
但是我們有很多的應用其實是需要存取整個系統的.
比如常用的bash script, 我們會直接存取系統上的資源或是直接呼叫另一個存在系統中的程式.
一般的snap發布時會自動review,但是classic confinement的snap需要管理人員人工審查.
畢竟這個功能會有一些安全上的疑慮.

https://github.com/shawn111/tmux.snap/blob/master/snapcraft.yaml

{% highlight yaml %}
name: xxx
version: 0.1
confinement: classic

...
{% endhighlight %}


另外一個top level commands(alias), 我還沒實際試過.
舉個例子lxd snap裡面有兩個command,
lxd 與 lxc, 而lxd因為跟snap名稱一樣, 所以還是lxd.
但是lxc就會變成lxd.lxc

想要嘗鮮嗎?
請把snapd升級到[2.20](<https://lists.snapcraft.io/archives/snapcraft/2016-December/002095.html>)

如果使用ubuntu zesty(17.04)現在就能用了,
如果是ubuntu xenial(16.04)目前還在proposed階段,可能還要過幾天才進xenial-update.

還不知道怎麼包snap嗎? 請詳見 http://snapcraft.io/
