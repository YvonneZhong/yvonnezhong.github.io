---
title: 'How to Create a New Page with HTML, CSS and JS Files'
tags:
  - Hexo
  - NexT
  - Blog
categories:
  - Hexo
date: 2020-05-13 15:34:33
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

## Create a new HTML Page
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
  # custom pages
  project1: /project1/ || fa fa-code
```

## Customize the Page Style
First, let's add two buttons in `index.html`:

```html
<body>
    <h2>This is the Project1 Page in HTML.</h2>
    <button class="button is-primary">Bulma</button>
    <button class="btn btn-primary">Bootstrap</button>
</body>
```

Then the page shows like this:
![image](https://live.staticflickr.com/65535/49888472773_b32c9f51c8_w_d.jpg)

Notice that, buttons display in different ways. This is because `btn` and `btn-primary` are the predesigned styles in `NexT` theme, which is a little tricky as they are assigned the same class name as `Bootstrap`. So, pay more attention if you plan to use `Bootstrap` in the future, as other parts, like sidebar, may also be changed.

Now, let's try to add separated css and js files to see whether it can work well.
```html project1/index.html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Project1</title>
</head>
<body>
    <h2>This is the Project1 Page in HTML.</h2>
    <button class="button is-primary" onclick="sayHello()">Bulma</button>
    <button class="btn btn-primary">Bootstrap</button>
    <script src="script.js"></script> 
</body>
</html>
```

```css project1/style.css
.button, .btn-primary {
    background-color: #3298dc;
    border-color: transparent;
    color: #fff;
}
```

```js project1/script.js
function sayHello() {
    alert('Hello, there.');
}
```

Results:
![image](https://live.staticflickr.com/65535/49888523058_3b7ddd54c5_w_d.jpg)

### Remove the ToC
Generally, the layout of `page` pages are defined in `themes/next/layout/page.swig`. So, go there to change the default layout of a page if necessary. Here, I just removed the `Table of Contents` in the sidebar by modify the code at the bottom of the file.

```swig 
{% block sidebar %}
  {{ sidebar_template.render(false) }}
{% endblock %}
```

Great, we successfully build a customized page so far.
However, this page is actually rendered from the template. If you don't like it, just skip the render:
```yml ./_config.yml
skip_render:
- "project1/**"
```

{% note info %}
"filename/*" - all the files in `filename` folder
"filename/**" - all the folders and files in `filename` folder
"filename/**/*" - all the folders in `filename` folder and files in both `filename` folder and subfolders
{% endnote %}

Clean the Hexo and restart the server, you can see your new page without any predesigned styles of NexT.
![image](https://live.staticflickr.com/65535/49889468267_9d5801739b_w_d.jpg)












