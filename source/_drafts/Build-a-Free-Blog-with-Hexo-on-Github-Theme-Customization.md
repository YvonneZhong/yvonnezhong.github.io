---
title: Build a Free Blog with Hexo on Github - Theme Customization
date: 2020-05-06 11:03:55
tags:
  - Hexo
  - Github
  - Blog
categories:
  - Hexo
description:
---
## Change Theme
### Hexo Theme
In the project folder, there is a directory called `themes` where you can store your theme folder in it. Modify the `theme` value in your site's `_config.yml`. A typical struction of a theme should like this:
```
.
├── source           // your assets (e.g. CSS and JS files)
├── languages
├── layout           // theme's template files
├── scripts
└── _config.yml      // Theme configuration file
```
<!-- more -->
### Change to Next Theme
Go to your site folder and clone the `Next Theme`:
```bash
$ git clone https://github.com/theme-next/hexo-theme-next themes/next
```
or you can manually download the `NexT Theme` files and locate it in `/theme` folder of your project.

Then modify the `theme` value in your site's `_config.yml`
```yml
theme: next
```
{% note danger %}
Remember to restart the server after modify your site's config file.
{% endnote %}

Refresh the page, your site with new theme should show up.

![image](https://live.staticflickr.com/65535/49861076306_7fab9993ed_w_d.jpg)

## Basic Settings
### Complete Site's Basic Info
Edit some basic infomation of your site. 

```yml _config.yml
# Site
title: Your Site Title
subtitle: Your site's subtitle
description: something about you or your site
keywords: keyword1, keyword2
author: your name
language: en  # set values according to next/languages
timezone: ''  # the same as your computer by default
```
These information will show on your site's sidebar.

![image](https://live.staticflickr.com/65535/49861237301_74e8fdcb8f_w_d.jpg)

### Theme Scheme
Users can change the settings of themes to custom the appearance of their blog by editing '_config.yml` file under the theme folder.

Four scheme options are offered in `NexT` theme, comment out the one you liked.
  
  ```yml ./themes/next/_config.yml
  # Schemes
  #scheme: Muse
  #scheme: Mist
  #scheme: Pisces
  scheme: Gemini
  ```

### Menu
Menu is the navigation of the blog that shows in the sidebar just below your site's titles. Edit the `menu settings` in theme configuration file to customize it.

```yml ./themes/next/_config.yml
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

To define a menu item, four parts are included: `key (the name of the menu item)`, `the target link`, `||` and the icon name (Font Awesome icon).

After settings, the menu shows like this:

![image](https://live.staticflickr.com/65535/49862487197_ddab944464_w_d.jpg)

However, when click the item of the menu, like `Tags`, the page shows `Cannot GET /tags/` error. That's because the `tags` page is not exist.

### Create New Pages
In your site's folder, input the command:
```bash
$ hexo new page tags
```
A new folder called `tags` will be created in `./source` with an `index.md` in it.

The same way can be applied to build `categories`, `archives` and `about` pages.

### Sidebar Settings
Find `sidebar` in `./themes/next/_config.yml`, then you can set sidebar's position, width and other information. 

### Favicon of Your Site
Select the image that you'd like to use as the favicon and put it in `./themes/nex/source/images`. Now change the favico setting in theme config file:
```yml
favicon:
  # small: /images/favicon-16x16-next.png
  medium: /images/owl-favicon.ico
  # apple_touch_icon: /images/apple-touch-icon-next.png
  # safari_pinned_tab: /images/logo.svg
```

### Footer of Site
```yml ./themes/nex/source/images
footer:
  since: 2020  # when the site was setup
  icon:  # between year and copyright info
    name: fa fa-heart  # name in Font Awesome
    animated: false  # icon display
    color: "#ff0000"  # color of the icon
  copyright: Yvonne Zhong  # owner of the copyright

  powered: true  # whether show powered by info
```
The footer displays like this:

![image](https://live.staticflickr.com/65535/49864523626_e83570d79f_w_d.jpg)

### Add Social info to Navbar
You can select which social information you want to show on your site. Comment out the line and change the links to your own social links.

```yml
GitHub: https://github.com/yourname || fab fa-github
#E-Mail: mailto:yourname@gmail.com || fa fa-envelope
#Twitter: https://twitter.com/yourname || fab fa-twitter
FB Page: https://www.facebook.com/yourname || fab fa-facebook
```

### Show Excerpt of the Post on the Homepage
Instead of display the whole content of posts, you can add `<!--more-->` in the post, then only the part before `<!--more-->` will show on the homepage with a `Read more` button.

![image](https://live.staticflickr.com/65535/49864096103_25d2735303_w_d.jpg)

{% note info %}
If the post has a description, then the description will be used as the excerpt of the post shown on the homepage.
{% endnote %}

Now, after these basic infomation have been set up, you can continue to write posts locally or deploy your blog on to the GitHub Pages.



  
