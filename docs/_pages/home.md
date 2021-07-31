---
permalink: /
title: "Tim Roith"
layout: single
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/img/Vision_2.png
  caption: "Me, a cat and some stuff."
excerpt: "My Personal site."
classes: wide
# sidebar:
#   - title: "Title"
#     image: "/assets/img/TecoNCat.jpg"
#     image_alt: "image"
#     text: "Some text here."
#   - title: "Another Title"
#     text: "More text here." 
---

# Introduction
Hi,
I'm Tim and this is my website. 

This place is used as a hybrid of self organization and public presentation of some projects I did in an academic context.  

# Posts
{% for post in site.posts limit: 5 %}
  {% include archive-single.html %}
{% endfor %}