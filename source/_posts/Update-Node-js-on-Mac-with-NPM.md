---
title: Update Node.js on Mac with NPM
tags:
  - Node.js
categories:
  - Node.js
date: 2020-05-16 12:55:42
description:
---

1. Check the current version that you are using on Mac

```bash
$ node -v
v13.3.0
```

2. Clean the npm cache (not sure if this is necessary)

```bash
$ npm cache clean --force
npm WARN using --force I sure hope you know what you are doing.

   ╭────────────────────────────────────────────────────────────────╮
   │                                                                │
   │      New patch version of npm available! 6.14.4 → 6.14.5       │
   │   Changelog: https://github.com/npm/cli/releases/tag/v6.14.5   │
   │               Run npm install -g npm to update!                │
   │                                                                │
   ╰────────────────────────────────────────────────────────────────╯
```

Update npm if you want.

3. Install `n` globally, which is a nodejs version management module.

```bash
$ npm install -g n
```

<!-- more -->

4. Now, you can update your Nodejs with `n`

```bash
$ sudo n latest  # update to the latest version
$ sudo n stable  # update to the stable version
```

Then input your password according to the instruction.

{% note danger %}
If you update to the latest version, other node-related apps may have issues.
{% endnote %}

5. Check the version

```bash
$ node -v  # v12.16.3 for the latest, v14.2.0 for the stable
```
