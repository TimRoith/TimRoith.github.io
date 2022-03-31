---
title: Publications and Presentations
layout: single
permalink: /publications/
#collection: publications
classes: wide
#entries_layout: grid
---
A list of my publications, preprints and presentations.

## Prints

{% assign entries_layout = page.entries_layout | default: 'list' %}

<div class="entries-{{ entries_layout }}">
  {% include publications-collection.html collection="publications"
     sort_by=page.sort_by sort_order=page.sort_order type=entries_layout status = "print" %}
</div>

## Preprints

<div class="entries-{{ entries_layout }}">
  {% include publications-collection.html collection="publications"
     sort_by="year" sort_order="year" type=entries_layout status = "preprint" %}
</div>

## Presentations

<div class="entries-{{ entries_layout }}">
  {% include publications-collection.html collection="publications"
     sort_by=page.year sort_order=page.year type=entries_layout status = "talk" %}
</div>
