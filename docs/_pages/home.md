---
permalink: /
title: "Tim Roith"
layout: single
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/img/Vision_2.png
  caption: "Me, a cat and some stuff."
excerpt: "My Personal Site."
classes: wide
# sidebar:
#   - title: "Title"
#     image: "/assets/img/TecoNCat.jpg"
#     image_alt: "image"
#     text: "Some text here."
#   - title: "Another Title"
#     text: "More text here." 
---

## Introduction

Hi,
I'm Tim and this is my website.

This place is used as a hybrid of self organization and public presentation of some projects I did in an academic context.  

## Recent Posts

{% for post in site.posts limit: 3 %}
  {% include archive-single.html %}
{% endfor %}

## Recent Publications

{% assign post_count = 0 %}
{% for post in site.publications %}
  {% if post.publication_info.status == "print" or post.publication_info.status == "preprint" %}
    {% assign post_count = post_count | plus: 1 %}
    {% include publication-single.html %}
  {% endif %}
  {% if post_count >= 3 %}
    {% break %}
  {% endif %}
{% endfor %}

## Recent Presentations

{% assign post_count = 0 %}
{% for post in site.publications %}
  {% if post.publication_info.status == "talk" %}
    {% assign post_count = post_count | plus: 1 %}
    {% include talk-single.html %}
  {% endif %}
  {% if post_count >= 3 %}
    {% break %}
  {% endif %}
{% endfor %}

## Relevant Links

* [List of publications](/publications/)
* [All posts](/posts-archive/)
