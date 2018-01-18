---
date: 2018-01-18
title: cli utilty to manage your github gist
---

Github Gist or PasteBin, it's kind of service allow you to post single files.
I found a nice cli utilty of Github Gist.

```
 $ go get github.com/b4b4r07/gist
```

*note, gist need fzf and peco to work*

```
 $ go get github.com/junegunn/fzf
 $ go get github.com/peco/peco
 $ cd $GOPATH/src/github.com/peco/peco
 $ make build
 $ cp releases/peco_linux_amd64/peco $GOPATH/bin/peco
```

config gist

```
 $ gist config
```

create new gist

```
 gist new <FILE_NAME>
```
