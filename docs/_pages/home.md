---
permalink: /
title: "Tim Roith"
layout: single
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/img/polar.gif
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

Hi, I'm Tim.
Currently I am a PhD student in mathematics at the Friedrich-Alexander Universität Erlangen-Nürnberg.

## Recent Posts

{% for post in site.posts limit: 6 %}
  {% include archive-single.html %}
{% endfor %}

## Recent Publications

{% assign sorted = site.publications | sort : "year" | reverse %}
{% assign post_count = 0 %}
{% for post in sorted %}
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
{% for post in sorted %}
  {% if post.publication_info.status == "talk" %}
    {% assign post_count = post_count | plus: 1 %}
    {% include talk-single.html %}
  {% endif %}
  {% if post_count >= 3 %}
    {% break %}
  {% endif %}
{% endfor %}

## Projects

{% assign entries_layout = "grid" | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% include documents-collection.html collection="projects" type=entries_layout %}
</div>
<hr style="clear:both;">

## Relevant Links

* [List of publications](/publications/)
* [All posts](/posts-archive/)
