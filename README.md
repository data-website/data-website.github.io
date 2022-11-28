# data-website


Our website has been deployed in [Github](https://github.com/data-website/data-website.github.io). The master branch is the source code of this website and the gh-pages branch is the code that generated from Hexo. I suggest that you can download the code from master branch and upload on another branch that named by your school or your name.

Our website is deployed in [https://data-website.github.io/](https://data-website.github.io/). Here are some introduction how to use this template.

## Installation

- <big>nodejs</big>

**The website to [download](https://nodejs.org/en/)**

- <big>hexo</big>

**Install hexo:**

``` bash
npm install -g hexo-cli
```

## Create in local path

Create hexo template. Create a new folder, `cd` in this folder

``` bash
hexo init
```

To use our website source code, you can only download the code from `master` branch. change **source, themes and _config.yml** files.


To check the website, run it in the local path.

``` bash
hexo g
```
hexo will generate the static file in `public` folder, to change the generated file, we can revise file in `source` folder. Then, we run the bash:

``` bash
hexo clean & hexo g
```

**run local server**

``` bash
hexo s
```

if has error, run the bash:

``` bash
npm install hexo-server --save
```

## Deploy in Github

**configure _config.yml**

```html
deploy:
  type: git
  repo: https://github.com/data-website/data-website.github.io.git
  branch: gh-pages # branch hexo generate
```

Run the bash:

```bash
hexo d
```

Hexo will deploy all files in `public` folder to ph-pages branch. Then the website is deployed in *username.github.io*

## New page

If the `source` directory doesn't have this file, you need to create a new one like this:

```bash
hexo new page "new page name"
```

When editing new page file *index.md*, need to add something

```markdown
title: new page name
date: 2018-09-30 17:25:30
type: "categories"
layout: "layout in theme"
```

## Modify Template



> **Note**: 