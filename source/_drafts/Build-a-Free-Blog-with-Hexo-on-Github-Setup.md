---
title: Build a Free Blog with Hexo on Github - Setup
date: 2020-05-06 10:33:08
tags:
- Hexo
- Github
- Blog
categories:
- Hexo
description:
---

Hexo is a fast, simple and powerful blog framework which is powered by Node.js. As Hexo support Markdown, it has been widely used to deploy a blog or other websites on Github Pages.

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
|   ├── draft.md         // draft scaffold
|   ├── page.md          // page scaffold
|   └── post.md          // post scaffold
├── source             // content of your site, like posts, img...
|   └── _posts           // theme folder
├── themes             // theme folder
|   └── landscape        // this is the default theme
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
 


