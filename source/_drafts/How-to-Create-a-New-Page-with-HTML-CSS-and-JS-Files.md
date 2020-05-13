---
title: 'How to Create a New Page with HTML, CSS and JS Files'
tags:
  - Hexo
  - NexT
  - Blog
categories:
  - Hexo
description:
---

The NexT theme comes with some basic pages, like `home`, `about`, `tags` and so on, which you can check and configure in `themes/next/_config.yml` like this: 

```yml
menu:
  home: / || fa fa-home
  about: /about/ || fa fa-user
  tags: /tags/ || fa fa-tags
  categories: /categories/ || fa fa-th
  archives: /archives/ || fa fa-archive
  #schedule: /schedule/ || fa fa-calendar
  #sitemap: /sitemap.xml || fa fa-sitemap
  #commonweal: /404/ || fa fa-heartbeat
```

As a programmer, recently, I'm thinking of building some customized pages with css and js files to display my portfolios or projects. If you have the similar thoughts to me, this post may give you some tips.

<!-- more -->

## Create a New Page
```bash
$ hexo new page project1
```

Then under the `/source` folder, a new folder called `project1` will be created with a `index.md` file in it. Edit the `index` file if you'd like to create your new page with markdown language. 

```md
---
title: Project1
date: 2020-05-13 11:49:26
---

## This is the Project1 Page in .md
```

Input `http://localhost:4000/project1/`, the Project1 page should look like this:

![image](https://live.staticflickr.com/65535/49888154693_0913e2c895_w_d.jpg)

But in my case, I will write the page in `HTML`. So, delete the `index.md` and in the `project1` folder, create an `index.html` file.

```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Project1</title>
</head>
<body>
    <h2>This is the Project1 Page in HTML.</h2>   
</body>
</html>
```

Now, start the hexo server locally, direct to url `http://localhost:4000/project1/` and you can view your new blank page only with the title on it.  

![image](https://live.staticflickr.com/65535/49888181098_c3cfaf4ffa_w_d.jpg)

## Add link on Navbar
Configure the theme config file to add the link of the new page on Navbar if you want.
```yml

```

