---
layout: page
title: Opera & Performance
nav_name: Opera
permalink: /portfolio/
description:
nav: true
nav_order: 3
---

<style>
  .video-portfolio {
    max-width: 1100px;
    margin: 0 auto;
  }

  .video-columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.25rem;
  }

  /* Clipping window — the "projector gate" */
  .video-col {
    overflow: hidden;
    height: 82vh;
    position: relative;
  }

  /* Soft fade at top and bottom edges — film-strip feel */
  .video-col::before,
  .video-col::after {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    height: 80px;
    z-index: 2;
    pointer-events: none;
  }

  .video-col::before {
    top: 0;
    background: linear-gradient(to bottom, var(--global-bg-color) 0%, transparent 100%);
  }

  .video-col::after {
    bottom: 0;
    background: linear-gradient(to top, var(--global-bg-color) 0%, transparent 100%);
  }

  /* The scrolling strip */
  .video-col-inner {
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
    will-change: transform;
  }

  .video-col-left .video-col-inner {
    animation: filmUp 28s linear infinite;
  }

  .video-col-right .video-col-inner {
    animation: filmDown 28s linear infinite;
    /* start at midpoint so columns are visually offset */
    animation-delay: -14s;
  }

  /* Cursor hint while hovering */
  .video-col:hover {
    cursor: ns-resize;
  }

  /* CSS animation as no-JS fallback only */
  @keyframes filmUp {
    0%   { transform: translateY(0); }
    100% { transform: translateY(-50%); }
  }

  @keyframes filmDown {
    0%   { transform: translateY(-50%); }
    100% { transform: translateY(0); }
  }

  .video-card {
    border-radius: 12px;
    overflow: hidden;
    background: #000;
    border: 1px solid rgba(255, 255, 255, 0.08);
    flex-shrink: 0;
    transition: box-shadow 0.25s ease;
  }

  .video-col:hover .video-card:hover {
    box-shadow: 0 10px 36px rgba(0, 0, 0, 0.55);
  }

  .video-wrapper {
    position: relative;
    padding-bottom: 56.25%;
    height: 0;
    overflow: hidden;
  }

  .video-wrapper iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
  }

  @media (max-width: 640px) {
    .video-columns {
      grid-template-columns: 1fr;
    }

    .video-col {
      height: auto;
      overflow: visible;
    }

    .video-col::before,
    .video-col::after {
      display: none;
    }

    /* On mobile: show static list, hide duplicates */
    .video-col-inner {
      animation: none;
    }

    .video-col-right .video-col-inner {
      animation: none;
    }

    .video-duplicate {
      display: none;
    }
  }
</style>

<div class="video-portfolio">
  <div class="video-columns">

    <!-- Left column: scrolls UP -->
    <div class="video-col video-col-left">
      <div class="video-col-inner">

        <!-- Original set -->
        <div class="video-card">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/h7CCMny7rqI" title="Performance 1"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/i0bu6Eizo8U" title="Performance 3"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/bAPj1S69O2c" title="Performance 5"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/J_g5P9xa074" title="Performance 7"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>

        <!-- Duplicate set for seamless loop -->
        <div class="video-card video-duplicate">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/h7CCMny7rqI" title="Performance 1"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card video-duplicate">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/i0bu6Eizo8U" title="Performance 3"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card video-duplicate">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/bAPj1S69O2c" title="Performance 5"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card video-duplicate">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/J_g5P9xa074" title="Performance 7"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>

      </div>
    </div>

    <!-- Right column: scrolls DOWN -->
    <div class="video-col video-col-right">
      <div class="video-col-inner">

        <!-- Original set -->
        <div class="video-card">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/aBZVmhbrerA" title="Performance 2"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/XgpBS4FTfFs" title="Performance 4"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/IfHzkWCyGKA" title="Performance 6"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/e34zCtESn_o" title="Performance 8"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>

        <!-- Duplicate set for seamless loop -->
        <div class="video-card video-duplicate">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/aBZVmhbrerA" title="Performance 2"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card video-duplicate">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/XgpBS4FTfFs" title="Performance 4"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card video-duplicate">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/IfHzkWCyGKA" title="Performance 6"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
        <div class="video-card video-duplicate">
          <div class="video-wrapper">
            <iframe src="https://www.youtube.com/embed/e34zCtESn_o" title="Performance 8"
              loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>

      </div>
    </div>

  </div>
</div>

<script>
(function () {
  if (window.innerWidth <= 640) return;

  var SPEED = 0.038; // px per ms for auto-scroll

  function initCol(col) {
    var inner = col.querySelector('.video-col-inner');
    var isRight = col.classList.contains('video-col-right');

    // Take over from CSS animation
    inner.style.animation = 'none';

    var y = 0;
    var velocity = 0;
    var hovered = false;
    var lastT = null;
    var halfH = 0;

    function measure() {
      halfH = inner.scrollHeight / 2;
      // Right column starts midway through its loop (matches the visual offset)
      if (isRight && y === 0) y = -halfH / 2;
    }

    function wrap(v) {
      if (halfH === 0) return v;
      while (v < -halfH) v += halfH;
      while (v > 0)      v -= halfH;
      return v;
    }

    function tick(t) {
      if (!lastT) lastT = t;
      var dt = Math.min(t - lastT, 50); // cap to avoid jumps after tab switch
      lastT = t;

      if (halfH === 0) measure();

      if (!hovered) {
        // Auto-roll: left goes up (−), right goes down (+)
        y += (isRight ? 1 : -1) * SPEED * dt;
        velocity = 0;
      } else {
        // Manual: apply inertia velocity
        y += velocity;
        velocity *= 0.84; // friction
        if (Math.abs(velocity) < 0.05) velocity = 0;
      }

      y = wrap(y);
      inner.style.transform = 'translateY(' + y + 'px)';
      requestAnimationFrame(tick);
    }

    col.addEventListener('mouseenter', function () { hovered = true; });
    col.addEventListener('mouseleave', function () { hovered = false; velocity = 0; });

    col.addEventListener('wheel', function (e) {
      if (!hovered) return;
      e.preventDefault();
      e.stopPropagation();
      // Natural scroll: wheel down → content moves up → negative delta
      velocity -= e.deltaY * 0.45;
      // Cap so it doesn't fly away
      velocity = Math.max(-28, Math.min(28, velocity));
    }, { passive: false });

    // Wait one frame so scrollHeight is measured after layout
    requestAnimationFrame(function () {
      measure();
      requestAnimationFrame(tick);
    });
  }

  document.querySelectorAll('.video-col').forEach(initCol);
})();
</script>
