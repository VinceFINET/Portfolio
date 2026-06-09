---
layout: default
title: Vincent's Art Portfolio
description: Vincent's Paintings and illustrations — acrylic on canvas, ink on paper.
permalink: /
---

<section class="home-hero">
  <h1 class="home-hero__title">{{ site.title }}</h1>
  <p class="home-hero__subtitle">{{ site.description }}</p>
</section>

<section class="home-collections" aria-label="Collections">
  <a href="{{ '/acrylic/' | relative_url }}" class="collection-card">
    <div class="collection-card__bg"
         style="background-image: url('{{ '/assets/img/IllustrationAcrylic.png' | relative_url }}')">
    </div>
    <div class="collection-card__body">
      <h2 class="collection-card__title">Acrylic Paintings</h2>
      <span class="collection-card__meta">9 works</span>
    </div>
  </a>

  <a href="{{ '/inktober/' | relative_url }}" class="collection-card">
    <div class="collection-card__bg"
         style="background-image: url('{{ '/assets/img/IllustrationInktober.png' | relative_url }}')">
    </div>
    <div class="collection-card__body">
      <h2 class="collection-card__title">Inktober</h2>
      <span class="collection-card__meta">Inktober 2025: 31 daily and 18 weekly drawings over the year 2025</span>
    </div>
  </a>
</section>
