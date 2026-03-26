---
layout: default
title: Research
permalink: /research/
---

<section class="page-hero page-hero--compact">
  <p class="eyebrow">RESEARCH</p>
  <h1>SPATIOTEMPORAL DYNAMICS OF INFLAMMATION</h1>
  <p class="muted"><strong>CLICK ON THE GREY ICONS FOR MORE DETAILS.</strong></p>
</section>

<section class="section">
  <div class="section-head">
    <div>
      <p class="eyebrow">OVERVIEW</p>
      <h2>RESEARCH FRAMEWORK</h2>
    </div>
  </div>
  <div class="stack-list">
    {% for item in site.data.research %}
      <article class="stack-card">
        <h3>{{ item.title | upcase }}</h3>
        <p>{{ item.summary }}</p>
        <ul>
          {% for bullet in item.bullets %}
            <li>{{ bullet }}</li>
          {% endfor %}
        </ul>
      </article>
    {% endfor %}
  </div>
</section>
