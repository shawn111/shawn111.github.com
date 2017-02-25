---
layout: post
title:  "nextcloud 第一個讓我有感的snap package"
date:   2017-02-20 10:20:28 +0800
tags: [snap, nextcloud]
---

這兩天與朋友聊到,有個多人分享的需求,
當然身為Ubuntu粉的我就給nextcloud當推薦了.

用來當私有的dropbox真不錯

nextcloud - 分家版的owncloud,選用nextcloud有一個特點nextcloud並沒有特別分enterprice版本,所有功能,
並且已經有現成的linux/win/android client


安裝
```
 # snap install nextcloud
```

環境設定, 網頁版就用browser 登入 http://localhost, 一開始會要求設定admin帳號密碼.

其他CLI 設定
```
 # nextcloud.occ
 # nextcloud.enable-https lets-encrypt # 除了enable https 連lets-encrpt的設定都好了
```

啥咪...這樣就好了?
yes...沒錯

事實上除了 nextcloud 已經有snap版外, [An Ubuntu snap-based solution for enterprises to control their data](<https://insights.ubuntu.com/2017/02/22/an-ubuntu-snap-based-solution-for-enterprises-to-control-their-data/?utm_content=buffer3133a&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer>)
