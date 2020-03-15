---
title: "Learning Notes For CSS"
header:
  teaser: "/assets/images/Code-Product-Landing.jpg"
excerpt_separator: "<!--more-->"
categories:
  - Web design
tags:
  - FreeCodeCamp
  - CSS
  - HTML
---

I used to design webpages for hosting Taiwan Ocean Science Meeting Events while I worked at Academic Sinica, Taipei (7 years ago). So, CSS is not completely new to me. Given that CSS has changed quite substantially in the last few years, participating the [Product Landing Project](https://codepen.io/michellechlin/full/mdJEVOv) in **FreeCodeCamp** is really good for myself to refresh the knowledge.
> Even if CSS is very small part of what I need to do.

I know I did not need to memorize every CSS syntax and values; however, making notes will make CSS much easier to use in the future.

## CSS Layout - float and clear  

`float` is used to positioning and formatting content.

`clear` is used to specify what elements can float beside the cleared element and on which side.

`box-sizing` defines how width and height of the element

`overflow` specifies what happens if content overflows an elements's box

`clearfix` works well when you want to control the margins and padding

`::after` is pseudo-element


 ```
 <style>
* {  
  box-sizing: border-box;
}

.image-container {
  float: left;
  width: 50%; /*for two images*/
  padding: 5px; /* build space between the images */
}

.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
```
##

## Resources for future uses:
- [w3schools](https://www.w3schools.com/default.asp)
- [HTML Color Code](https://htmlcolorcodes.com/color-chart/)
