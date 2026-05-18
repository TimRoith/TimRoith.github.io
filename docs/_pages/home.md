---
permalink: /
title: "Hi, I'm Tim!"
layout: single
#header:
  #overlay_color: "#000"
  #overlay_filter: "0.5"
#  overlay_image: /assets/img/polar.gif
#  caption: "The magic of PolarCBO."
#  actions:
#  - label: "Visualization via PolarCBO"
#    url: "https://github.com/TimRoith/polarcbo"
#classes: wide
# sidebar:
#   - title: "Title"
#     image: "/assets/img/TecoNCat.jpg"
#     image_alt: "image"
#     text: "Some text here."
#   - title: "Another Title"
#     text: "More text here." 
---

I'm currently a substitute professor at the [Technical University of Munich](https://campus.tum.de/tumonline/visitenkarte.show_vcard?pPersonenGruppe=3&pPersonenId=DB0D4E7C32EE1BB1). I am a member of the [COST Action InterCoML](https://www.cost.eu/actions/CA24136/) and the [Munich Center for Machine Learning](https://mcml.ai/research/groups/fornasier/).

My research lies at the intersection of mathematical analysis, optimization, and machine learning. I work on consensus-based optimization methods, robustness and stability of neural networks, and learning problems in imaging and inverse problems.

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
