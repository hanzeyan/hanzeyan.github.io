---
layout: default
title: Resources
permalink: /resources/
---

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
