---
title: Build a Free Blog with Hexo on Github - Optimization
tags:
  - Hexo
  - Github
  - Blog
categories:
  - Hexo
description:
---

## Set Canvas-nest as the Background
Create a file named footer.swig in hexo/source/_data directory (create _data directory if it does not exist).
```html
<script color="0,0,255" opacity="0.5" zIndex="-1" count="99" src="https://cdn.jsdelivr.net/npm/canvas-nest.js@1/dist/canvas-nest.js"></script>
```
In the NexT _config.yml, uncomment footer under the custom_file_path section.
```yml
custom_file_path:
  #head: source/_data/head.swig
  #header: source/_data/header.swig
  #sidebar: source/_data/sidebar.swig
  #postMeta: source/_data/post-meta.swig
  #postBodyEnd: source/_data/post-body-end.swig
  footer: source/_data/footer.swig
  #bodyEnd: source/_data/body-end.swig
  #variable: source/_data/variables.styl
  #mixin: source/_data/mixins.styl
  #style: source/_data/styles.styl
```

Learn more: https://github.com/theme-next/theme-next-canvas-nest
<!-- more -->

## Add Statistics
```yml ./themes/next/_config.yml
busuanzi_count:
  enable: true
  total_visitors: true
  total_visitors_icon: fa fa-user
  total_views: true
  total_views_icon: fa fa-eye
  post_views: true
  post_views_icon: fa fa-eye
```

## Add word count and time to read for articles

```bash
$ npm install hexo-symbols-count-time --save
```

```yml /next/_config.yml
symbols_count_time:
  separated_meta: true
  item_text_post: true
  item_text_total: false
```

```yml ./_config.yml
symbols_count_time:
  awl: 5  # Average Word Length CN-2, EN-5
  wpm: 200  # 200~250
  symbols: true
  time: true
  total_symbols: true
  total_time: true
  exclude_codeblock: false
  suffix: "mins."
```
