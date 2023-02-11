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

## Add new dataset

To add a new block in data&API page, just change the `JSON` sequence in `data&APIs.ejs`. The `JSON` sequence is at the bottom of this page, inside the `<script>`. The format is as follows:

```bash
 var arr=[
    {class:'1',category:"RFID", application:"Recognition", src: "/medias/images/data&APIs/RFID_BioTag.png", date:'Feb.2 2023', href: "https://zenodo.org/record/7466946#.Y96Qa3aZMSE",subtitle: "RFID-based User Verification",name:"BioTag",introduction:"BioTag RFID dataset is initially collected for continuous user verification. The dataset contains raw RFID samples from two RFID tags attached to the chest and abdomen of 10 participants. The RFID samples capture users' unique physiological characteristics, such as heartbeat and respiration patterns.",home_introduction:"BioTag is an RFID dataset originally collected for continuous user authentication based on unique biometrics in human respiration patterns. This dataset contains RFID raw data samples collected from two RFID tags attached to the chest and abdomen of 10 participants."},
 ]
 ```
 
 `class` represents the application of this block, `1` represents it's a dataset. `2` represents it's an application. 
`src` is the location of image. The path of image `/medias/images/data&APIs/`. 
`href` is the website where to download the dataset.
`intoduction` is to introduce this dataset on the `Data&APIs` page.
`home_introduction` is to introduce this dataset on the `Home` page.

The whole path to adding an image is `themes/hexo-theme-matery-develop/source/medias/images/data&APIs/`. Please chage the `JSON` sequence in `home.ejs` page at the same time. The `JSON` sequence is also inside the `<script>` at the bottom of the page.

## Add a block in `Timeline` page

Add a new `.md` file in the path of `source/_posts`, the format is as follows:

```bash
---
name: BioTag
title: RFID-based User Verification
date: 2023-1-15
href: https://zenodo.org/record/7466946#.Y96Qa3aZMSE
imgsrc: /medias/images/data&APIs/RFID_BioTag.png
introduction: BioTag is an RFID dataset originally collected for continuous user authentication based on unique biometrics in human respiration patterns. This dataset contains RFID raw data samples collected from two RFID tags attached to the chest and abdomen of 10 participants.
contributor: Temple University
---
```


> **Note**: Please let us know after updating some pages. Thank you.