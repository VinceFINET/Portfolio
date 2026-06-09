---
layout: default
title: Art Portfolio
description: Paintings and illustrations — acrylic on canvas, ink on paper.
permalink: /
---

<section class="home-hero">
  <h1 class="home-hero__title">{{ site.title }}</h1>
  <p class="home-hero__subtitle">{{ site.description }}</p>
</section>

<section class="home-collections" aria-label="Collections">
  <a href="{{ '/acrylic/' | relative_url }}" class="collection-card">
    <div class="collection-card__bg"
         style="background-image: url('{{ '/assets/img/Acrylic-BeigeLeaves.jpg' | relative_url }}')">
    </div>
    <div class="collection-card__body">
      <h2 class="collection-card__title">Acrylic Paintings</h2>
      <span class="collection-card__meta">9 works</span>
    </div>
  </a>

  <a href="{{ '/inktober2025/' | relative_url }}" class="collection-card">
    <div class="collection-card__bg"
         style="background-image: url('{{ '/assets/img/Inktober2025-week01.jpg' | relative_url }}')">
    </div>
    <div class="collection-card__body">
      <h2 class="collection-card__title">Inktober 2025</h2>
      <span class="collection-card__meta">31 days &middot; 18 compilations</span>
    </div>
  </a>
</section>
