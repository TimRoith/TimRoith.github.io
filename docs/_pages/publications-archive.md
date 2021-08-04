---
title: Publications
layout: single
permalink: /publications/
#collection: publications
classes: wide
#entries_layout: grid
---
A list of my publications. In order to add to the exsisting troubles of publication taxinomy 
this list is not connected to any other public services. In fact, right now I write these entries 
by hand. This is not optimal, but due to the co-existence of different established sites 
somewhat consistent. Here is a collection of important sites that also keep track of publications.

|Provider                                   | My Profile      |
|:-----------------------------------------:|:---------------:|
|CRIS, in-house system of FAU | [Tim Roith CRIS](https://cris.fau.de/converis/portal/Person/221675131?auxfun=&lang=en_GB) |
| ORCID                                     | ID: 0000-0001-8440-2928 |
| Researchgate                              | [Tim Roith RG](https://www.researchgate.net/profile/Tim-Roith) |
| Google Scholar                            | [Tim Roith Google Scholar](https://scholar.google.com/citations?user=BKlbQTAAAAAJ&hl=en)

## Prints
{% assign entries_layout = page.entries_layout | default: 'list' %}

<div class="entries-{{ entries_layout }}">
  {% include publications-collection.html collection="publications" 
     sort_by=page.sort_by sort_order=page.sort_order type=entries_layout status = "print" %}
</div>

## Preprints
<div class="entries-{{ entries_layout }}">
  {% include publications-collection.html collection="publications" 
     sort_by=page.sort_by sort_order=page.sort_order type=entries_layout status = "preprint" %}
</div>

## Presentations
<div class="entries-{{ entries_layout }}">
  {% include publications-collection.html collection="publications" 
     sort_by=page.sort_by sort_order=page.sort_order type=entries_layout status = "talk" %}
</div>