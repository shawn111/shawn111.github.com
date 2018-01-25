---
date: 2018-01-19
title: use git worktree/submodule and CI to create hugo github-pages
tags: 
 - "git"
 - "github"
 - "github-pages"
 - "CI"
---

As begin, I confused about the github-pages rules.
I found git worktree/submodule are so great to keep your github-pages repo clear.

You might need below type of branch or repo

 * public data branch: git worktree (*master* or *gh-pages*)
 * source data branch (maybe branch *hugo*)
 * theme repo as git submodule

Once you split your repo structure, you can add CI.
Then you can just force about content and don't need to care about the public parts.
CI will automatic generate it for you.

## github-pages repo and branch rules
### personal, organization github-pages repo: specific rule

```
repo name: *<user/organization>.github.io*
branch: master
url: shawn111.github.io
```

To host personal, organization: *<user/organization>.github.io*

example for myself: shawn111.github.io

### other repos
I recommend just use branch gh-pages, or you can refer https://pages.github.com/ if you want use master branch.

```
repo name: repo
branch: gh-pages
url: shawn111.github.io
```



