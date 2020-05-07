---
title: >-
  no such file or directory, open
  &#39;themes&#92;next&#92;layout&#92;&#95;scripts&#92;schemes&#92;.swig&#39;
tags:
  - Trouble Shooting
  - Hexo
categories:
  - Hexo
date: 2020-05-07 12:07:10
description:
---



## Trouble
After adding social links in theme configuration file, Hexo throwed an error when execute `$ hexo deploy -g`:
```
Unhandled rejection Error: ENOENT, no such file or directory '/home/msy/MyBlog/themes/next/layout/_scripts/schemes/.swig'
```
<!-- more -->
## Solution
Comment out the `key` line as well when adding a new type setting.
```yml
social:
  Twitter: https://twitter.com/yourname || twitter
```


