---
date: 2018-01-25
title: How to speed up X11 forwarding in SSH
tags: 
 - "ssh"
 - "linux"
 - "gui"
---

vi ~/.ssh/config

```
Host remote_host.com
  Compression yes
  ForwardX11 yes
  Ciphers blowfish-cbc,arcfour
```

http://xmodulo.com/how-to-speed-up-x11-forwarding-in-ssh.html
