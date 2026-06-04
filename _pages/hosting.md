---
layout: page
title: Mandarin hosting & Recitation Highlights
nav_name: Hosting
permalink: /hosting/
description:
nav: true
nav_order: 4
---

<style>
  .video-gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 1.5rem;
    margin-top: 1.5rem;
  }

  .gallery-card {
    border-radius: 10px;
    overflow: hidden;
    background: var(--global-card-bg-color, #fff);
    border: 1px solid var(--global-divider-color, rgba(0, 0, 0, 0.1));
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    transition: box-shadow 0.2s ease, transform 0.2s ease;
  }

  .gallery-card:hover {
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
    transform: translateY(-3px);
  }

  .gallery-card .video-wrapper {
    position: relative;
    padding-bottom: 56.25%; /* 16:9 */
    height: 0;
    overflow: hidden;
    background: #000;
  }

  .gallery-card .video-wrapper iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
  }

  .gallery-card .caption {
    padding: 0.75rem 1rem;
    font-size: 0.95rem;
    line-height: 1.3;
    color: var(--global-text-color, #333);
  }
</style>

<!--
  To add a video: copy one .gallery-card block below and replace
  - the YouTube ID after /embed/  (e.g. .../embed/VIDEO_ID)
  - the title="" attribute
  - the caption text
  Delete any unused placeholder cards.
-->

<div class="video-gallery">

  <div class="gallery-card">
    <div class="video-wrapper">
      <iframe src="https://www.youtube.com/embed/m3-lmWTAhkQ" title="Falling Leaves (《落叶》) by Shu Ting | Chinese National Recitation Competition"
        loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="caption">《落叶》· 舒婷 — Recitation at the Chinese National Recitation Competition</div>
  </div>

  <div class="gallery-card">
    <div class="video-wrapper">
      <iframe src="https://www.youtube.com/embed/J1z7wu7wjC4" title="若我归来 | Mandarin Poetry Recitation"
        loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="caption">《若我归来》— Mandarin poetry recitation</div>
  </div>

  <div class="gallery-card">
    <div class="video-wrapper">
      <iframe src="https://www.youtube.com/embed/87uIlcHDKmc" title="Featured Audience Interaction with Lo Ta-yu (CCTV)"
        loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="caption">CCTV · 与罗大佑现场互动 — Featured audience interaction with Lo Ta-yu</div>
  </div>

  <div class="gallery-card">
    <div class="video-wrapper">
      <iframe src="https://www.youtube.com/embed/iOPolA6didM" title="Opera Talk: Die Fledermaus"
        loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="caption">歌剧导赏《蝙蝠》— Opera talk introducing Die Fledermaus</div>
  </div>

  <div class="gallery-card">
    <div class="video-wrapper">
      <iframe src="https://www.youtube.com/embed/mJhS5Rwrkf0" title="Mandarin Concert Hosting Sample | Introducing a Chinese Concerto"
        loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="caption">音乐会主持示范 · 介绍中国协奏曲 — Mandarin concert hosting sample</div>
  </div>

  <div class="gallery-card">
    <div class="video-wrapper">
      <iframe src="https://www.youtube.com/embed/BLgX_ZVwvKA" title="Event Hosting | Zhejiang Conservatory of Music Opening Ceremony"
        loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="caption">浙江音乐学院开学典礼 · 活动主持 — Event hosting at Zhejiang Conservatory of Music</div>
  </div>

</div>
