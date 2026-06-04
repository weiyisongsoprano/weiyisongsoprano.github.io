---
layout: page
title: Gallery
permalink: /gallery/
description:
nav: true
nav_order: 5
---

<style>
  /* Masonry layout — each photo shown at its full, uncropped aspect ratio */
  .photo-gallery {
    column-count: 3;
    column-gap: 1rem;
    margin-top: 1.5rem;
  }

  @media (max-width: 900px) {
    .photo-gallery { column-count: 2; }
  }

  @media (max-width: 560px) {
    .photo-gallery { column-count: 1; }
  }

  .photo-card {
    break-inside: avoid;
    margin-bottom: 1rem;
    border-radius: 10px;
    overflow: hidden;
    border: 1px solid var(--global-divider-color, rgba(0, 0, 0, 0.1));
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    transition: box-shadow 0.2s ease, transform 0.2s ease;
    background: var(--global-card-bg-color, #fff);
  }

  .photo-card:hover {
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
    transform: translateY(-3px);
  }

  .photo-card img {
    display: block;
    width: 100%;
    height: auto; /* full image, no cropping */
  }

  .photo-card .caption {
    padding: 0.6rem 0.9rem;
    font-size: 0.9rem;
    line-height: 1.3;
    color: var(--global-text-color, #333);
  }
</style>

<!--
  Photos are loaded automatically from assets/pics/.
  Drop new images into that folder and they will appear here on rebuild.
-->

<div class="photo-gallery">
  {% assign pics = site.static_files | where_exp: "f", "f.path contains '/assets/pics/'" | sort: "name" %}
  {% for pic in pics %}
    <div class="photo-card">
      <img src="{{ pic.path | relative_url }}" alt="{{ pic.basename }}" loading="lazy">
    </div>
  {% endfor %}
</div>
