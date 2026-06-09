---
layout: default
title: Inktober
description: Inktober is a drawing challenge
permalink: /inktober/
---

<header class="page-header">
  <h1 class="page-header__title">{{ page.title }}</h1>
  <p class="page-header__description">{{ page.description }}</p>
</header>

<section aria-labelledby="section-days">
  <div class="section-header">
    <h2 class="section-header__title" id="section-days">Inktober 2025 Daily Drawings</h2>
  </div>
  <div class="gallery-grid gallery-grid--dense" role="list">
  {% assign day_images = site.static_files
       | where_exp: "f", "f.path contains 'Inktober2025-day'"
       | sort: "name" %}
  {% for img in day_images %}
  {% assign caption = img.basename | split: "-" | last %}
    <a class="gallery-item glightbox"
       href="{{ img.path | relative_url }}"
       data-gallery="inktober-days"
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
</section>

<hr class="section-divider">

<section aria-labelledby="section-weeks">
  <div class="section-header">
    <h2 class="section-header__title" id="section-weeks">Inktober 2025 Weekly Drawings</h2>
  </div>
  <div class="gallery-grid gallery-grid--wide" role="list">
  {% assign week_images = site.static_files
       | where_exp: "f", "f.path contains 'Inktober2025-week'"
       | sort: "name" %}
  {% for img in week_images %}
  {% assign caption = img.basename | split: "-" | last %}
    <a class="gallery-item glightbox"
       href="{{ img.path | relative_url }}"
       data-gallery="inktober-weeks"
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
</section>
