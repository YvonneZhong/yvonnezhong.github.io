---
title: Build a Free Blog with Hexo on Github - Deploy to GitHub Pages
tags:
  - Hexo
  - Github
  - Blog
categories:
  - Hexo
description:
---

After setup and some basic customization, you are all set for your blog system with Hexo on your own computer. But how can we have our own blog site on the Internet where we could share it with others? GitHub Pages.

Now, why GitHub Pages?
- Free
- 1GB usage limit with 100GB soft bandwidth limit per month, which is quite enough if you will not put big-size files in it
- You can custom domain with your own domain

In this post, let's see how can we deploy the blog onto GitHub Pages.

<!-- more -->
## Signup GitHub Account

## Create a New Repository for your GitHub Pages

## Install hexo-deployer-git
```bash
$ npm install hexo-deployer-git --save
```

## Configuration
```yml ./_config.yml
url: https://yvonnezhong.github.io/  # change it to your name
```

## Create a New Branch for your Blog

## Deploy
```bash
$ hexo clean
$ hexo g
$ hexo d
```
Then you can view your own blog with `https://yourusername.github.io/`



