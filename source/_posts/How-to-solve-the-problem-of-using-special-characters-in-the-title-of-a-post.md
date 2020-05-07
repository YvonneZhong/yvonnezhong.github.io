---
title: How to solve the problem of using special characters in the title of a post
tags:
  - Hexo
  - HTML Character Codes
categories:
  - Hexo
date: 2020-05-07 14:20:30
description:
---


In most of the time, it works fine when using a special character like `/`, `'`, `[]` and ` ` in the title of an article just by enclosing them in a pair of double quotes.

However, when it comes across a `Backslash` (\\), things can be a little tricky.
<!-- more -->
Let's say you tend to create an article with command:
```bash
$ hexo new "open 'themes\next' files"
```
It seems that Hexo does create a draft or post for you successfully. However when we open the post, we see the title displayed in an odd way:
```markdown
---
title: |-
  open 'themes
  ext' files
tags:
  - null
categories:
  - null
---
```
So, we try to use `&#92;` instead, which is the HTML character code of backslash:
```bash
$ hexo new "open 'themes&#92;next' files"
```
A new post called `open-themes-92-next-files.md` was established with the following content:
```md
---
title: 'open ''themes&#92;next'' files'
tags:
  - null
categories:
  - null
description:
---
```
And how does the post display on the blog? 

![image](https://live.staticflickr.com/65535/49865436637_d821fa56e1_w_d.jpg)

Bingo!