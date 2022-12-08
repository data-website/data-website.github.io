---
title: Add data&APIs
---
To add a category, change the json sequence in `data&APIs.ejs`:

```bash
 var arr=[
    {category:"PPG", src: "/medias/featureimages/13.jpg", href: "/Data&APIs/index.html",introduction: "introduction"},
    {category:"RFID", src: "/medias/featureimages/13.jpg", href: "#",introduction: "introduction"},
    {category:"WiFi", src: "/medias/featureimages/13.jpg", href: "#",introduction: "introduction"}
 ]
 ```
 
 After cliking the card, you can link to another platform that restore the datasets or just create a new page by using this template. If use this template, create a md file in `source\_posts` files.
 To revise the template of this page, `post.ejs` and `\_partial\post-detail.ejs` are related. 
 `source\css\my.css` to add new css.
 
 `source\medias\images` to add figure.
 
 `index.ejs` is the home page, `bg-cover.ejs` to revise the background.