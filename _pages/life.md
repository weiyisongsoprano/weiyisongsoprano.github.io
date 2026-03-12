---
layout: page
title: What You See in Me
permalink: /life/
description: Echoes & Impressions
nav: true
nav_order: 7
---

<style>
  .impression-container {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
  }

  .input-section {
    background: var(--global-bg-color);
    border: 2px solid var(--global-divider-color);
    border-radius: 12px;
    padding: 30px;
    margin-bottom: 40px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  }

  .input-section h3 {
    margin-top: 0;
    margin-bottom: 15px;
    color: linen;
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.5rem;
    font-weight: 600;
    letter-spacing: 0.01em;
  }

  .input-section p {
    margin-bottom: 20px;
    color: var(--global-text-color);
    opacity: 0.8;
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem;
    line-height: 1.9;
    letter-spacing: 0.01em;
  }

  .input-group {
    display: flex;
    gap: 10px;
    margin-bottom: 15px;
  }

  #impressionInput {
    flex: 1;
    padding: 12px 16px;
    border: 2px solid var(--global-divider-color);
    border-radius: 8px;
    font-size: 16px;
    background: var(--global-bg-color);
    color: var(--global-text-color);
    transition: border-color 0.3s;
  }

  #impressionInput:focus {
    outline: none;
    border-color: var(--global-theme-color);
  }

  #submitBtn {
    padding: 12px 30px;
    background: var(--global-theme-color);
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
  }

  #submitBtn:hover {
    opacity: 0.9;
    transform: translateY(-1px);
  }

  #submitBtn:active {
    transform: translateY(0);
  }

  .word-count {
    font-size: 14px;
    color: var(--global-text-color);
    opacity: 0.6;
    text-align: right;
  }

  .cloud-section {
    background: var(--global-bg-color);
    border: 2px solid var(--global-divider-color);
    border-radius: 12px;
    padding: 40px;
    min-height: 400px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  }

  .cloud-section h3 {
    text-align: center;
    margin-top: 0;
    margin-bottom: 30px;
    color: var(--global-theme-color);
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.5rem;
    font-weight: 600;
    letter-spacing: 0.02em;
  }

  #wordCloud {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    gap: 15px;
    min-height: 300px;
    padding: 20px;
  }

  .word-item {
    display: inline-block;
    padding: 8px 12px;
    margin: 5px;
    cursor: default;
    transition: all 0.3s;
    border-radius: 6px;
    background: var(--global-code-bg-color);
    color: var(--global-theme-color);
    font-weight: 600;
    line-height: 1.2;
  }

  .word-item:hover {
    transform: scale(1.1);
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
  }

  .empty-state {
    text-align: center;
    color: var(--global-text-color);
    opacity: 0.5;
    padding: 60px 20px;
    font-size: 18px;
  }

  .stats-section {
    text-align: center;
    margin: 20px 0;
    padding: 15px;
    background: var(--global-code-bg-color);
    border-radius: 8px;
    font-size: 14px;
    color: var(--global-text-color);
  }

  .stats-section strong {
    color: var(--global-theme-color);
  }

  .note {
    margin-top: 20px;
    padding: 15px;
    background: var(--global-code-bg-color);
    border-left: 4px solid var(--global-theme-color);
    border-radius: 4px;
    font-size: 1rem;
    font-family: 'Cormorant Garamond', serif;
    line-height: 1.8;
    color: var(--global-text-color);
    opacity: 0.8;
  }

  @media (max-width: 768px) {
    .input-group {
      flex-direction: column;
    }
    
    #submitBtn {
      width: 100%;
    }

    .cloud-section {
      padding: 20px;
    }
  }
</style>

<div class="impression-container">
  <div class="input-section">
    <h3> What words or phrases come to mind when you think of me? </h3>
    
    <div class="input-group">
      <input 
        type="text" 
        id="impressionInput" 
        placeholder="Enter words or phrases (e.g., creative, innovative, helpful...)" 
        maxlength="100"
      />
      <button id="submitBtn">Add</button>
    </div>
    
    <div class="word-count">
      <span id="charCount">0</span> / 100 characters
    </div>

    <div class="note">
      💡 <strong>Tip:</strong> You can enter multiple words separated by commas, or submit one word at a time. If a word has more than one part (e.g., warm-smiling), connect the parts with a hyphen instead of a space.
    </div>
  </div>

  <div class="stats-section">
    <strong id="totalWords">0</strong> unique words · <strong id="totalSubmissions">0</strong> total submissions
  </div>

  <div class="cloud-section">
    <h3>☁️ Word Cloud</h3>
    <div id="wordCloud">
      <div class="empty-state">
        Be the first to share your impression! 🌟
      </div>
    </div>
  </div>
</div>

<!-- Firebase SDK -->
<script src="https://www.gstatic.com/firebasejs/9.22.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.22.0/firebase-database-compat.js"></script>

<script src="{{ '/assets/js/word-cloud.js' | relative_url }}"></script>

---

## 🌍 Visitors Around the World

<div class="globe-section">
  <div class="globe-wrapper">
    <script type="text/javascript" id="clstr_globe" src="//clustrmaps.com/globe.js?d=uzKn1_iPcr4O83gptLmo2I1y28EhQkGfoEbe1B1UOHY"></script>
  </div>
</div>

<style>
  .globe-section {
    max-width: 500px;
    margin: 4rem auto 2rem auto;
    text-align: center;
  }

  .globe-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    transform: scale(0.8);
    transform-origin: center top;
    margin-top: 0px;
  }
</style>
