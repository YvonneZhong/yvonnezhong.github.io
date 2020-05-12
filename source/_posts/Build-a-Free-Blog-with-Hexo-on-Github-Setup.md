---
title: Build a Free Blog with Hexo on Github - Setup
tags:
  - Hexo
  - Github
  - Blog
categories:
  - Hexo
date: 2020-05-06 10:33:08
description:
---



Hexo is a fast, simple and powerful static blog generating framework which is powered by Node.js. As Hexo support Markdown, it has been widely used to deploy a blog or other websites on Github Pages.

Before Hexo, I have tried several ways to build my technology blog on different platforms or servers, like blogger, wordpress.com or AWS ES2 with my own coded CMS.
However, none of them met my needs:
- Markdown is not only supported when writing, but also can display accordingly
- Simple theme that can be customized
- Easy to backup
- Safe enough

In this series, I will give some instructions about how to build a personal blog with Hexo and Github according to my hands-on practice.

<!-- more -->
## Install Hexo
```bash
$ npm install -g hexo-cli
```
{% note info %}
Make sure you have installed Node.js and Git before this step. 
{% endnote %}
## Initialize Hexo
Create a folder for the blog and initialize Hexo in that directory.
```bash
$ mkdir blog
$ cd blog
$ hexo init
```
The structure of the project folder will then look like this:
```
.
├── node_modules       // libraries downloaded from npm
├── scaffolds          // scaffold folder
|   ├── draft.md       // draft scaffold
|   ├── page.md        // page scaffold
|   └── post.md        // post scaffold
├── source             // content of your site, like posts, img...
|   └── _posts         // theme folder
├── themes             // theme folder
|   └── landscape      // this is the default theme
├── .gitignore         // unchecked git files
├── _config.yml        // Site configuration file
├── db.json            
├── package.json       // manifest of the project
└── package-lock.json
```

## Start Server
```bash
$ hexo s
```

Now, you can open http://localhost:4000 in your browser to check your own blog. It should like this:

![image](https://live.staticflickr.com/65535/49857419726_c9236debe7_w_d.jpg)

{% note info %}
Use Ctrl + C to quit server.
{% endnote %}
 


