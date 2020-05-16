---
title: "error: src refspec master does not match any"
tags:
  - Git
  - Trouble Shooting
categories:
  - Git
date: 2020-05-15 12:42:41
description:
---

## Trouble

When I execute `git push` command to push a new established folder to GitHub, it gave the error:

```bash
error: src refspec master does not match any
error: failed to push some refs to 'https://github.com/Username/Newfolder.git'
```

## Solution

After adding a file to that folder, everything worked fine.

## Reason

Git won't track `empty` repositories. So before push it to the remote, make sure that it is not empty.
