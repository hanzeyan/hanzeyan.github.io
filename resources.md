---
layout: default
title: Resources
permalink: /resources/
---

<section class="page-hero page-hero--feature">
  <div class="hero-copy">
    <p class="eyebrow">Resources</p>
    <h1>Lab Protocols</h1>
  </div>
  <div class="feature-image-wrap">
    <img src="{{ site.data.site.resources_hero_image }}" alt="Lab protocols" class="feature-image">
  </div>
</section>

<section class="section">
  <div class="resource-grid">
    {% for block in site.data.resources %}
      <article class="resource-card">
        <h3>{{ block.category }}</h3>
        {% if block.items.size > 0 %}
        <ul>
          {% for item in block.items %}
            <li>{{ item }}</li>
          {% endfor %}
        </ul>
        {% endif %}
      </article>
    {% endfor %}
  </div>
</section>
