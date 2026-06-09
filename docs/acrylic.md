---
layout: default
title: Acrylic Paintings
description: A collection of acrylic paintings exploring colour, light, and memory — from Normandy beaches to Marvel heroes.
permalink: /acrylic/
---

<header class="page-header">
  <h1 class="page-header__title">{{ page.title }}</h1>
  <p class="page-header__description">{{ page.description }}</p>
</header>

<div class="gallery-grid" role="list">
{% assign acrylic_images = site.static_files
     | where_exp: "f", "f.path contains 'Acrylic-'"
     | sort: "name" %}
{% for img in acrylic_images %}
{% assign caption = img.basename | split: "-" | last %}
  <a class="gallery-item glightbox"
     href="{{ img.path | relative_url }}"
     data-gallery="acrylic"
     data-title="{{ caption }}"
     role="listitem"
     aria-label="{{ caption }}">
    <img src="{{ img.path | relative_url }}"
         alt="{{ caption }}"
         loading="lazy">
    <span class="gallery-caption" aria-hidden="true">{{ caption }}</span>
  </a>
{% endfor %}
</div>
