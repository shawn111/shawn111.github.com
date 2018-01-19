---
date: 2018-01-18
title: cli utilty to manage your github gist
---

Github Gist or PasteBin, it's kind of service allow you to post single files.
For me, the only backdraw is Gist don't have a nice cli client.

I found a nice cli utilty of Github Gist. github.com/b4b4r07/gist


<!--more-->

Hers are some features Gist that better then PasteBin.

 * version control
 * could be private or public
 * github supported layout, like md like could be much readable

## install gist

### go get github.com/b4b4r07/gist
If you have no idea how to use go, you can refer some golang docs or [go-get-command](https://nanxiao.gitbooks.io/golang-101-hacks/content/posts/go-get-command.html)
```
 $ go get github.com/b4b4r07/gist
```

### extra commands that need to be installed

*note, gist need fzf and peco to work*

```
 $ go get github.com/junegunn/fzf
 $ go get github.com/peco/peco
 $ cd $GOPATH/src/github.com/peco/peco
 $ make build
 $ cp releases/peco_linux_amd64/peco $GOPATH/bin/peco
```
## config gist

Before you use gist, you need to create ~/.config/gist/config.toml first, *gist config* help you make it a lot easier.
You still need to [modify your own github token](https://github.com/settings/tokens).

```
 $ gist config
 # modify gist.token
```

create new gist

```
 $ gist new <FILE_NAME>

 $ cat <file> | gist new
Created https://gist.github.com/856fdb7bcdda0b478909f19e5489245d
Created new window in existing browser session.
```
