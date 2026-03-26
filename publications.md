---
layout: default
title: Publications
permalink: /publications/
---

<section class="page-hero page-hero--compact">
  <p class="eyebrow">PUBLICATIONS</p>
  <h1>PUBLICATIONS &amp; REVIEWS</h1>
  <p># denotes co-first authors; * denotes corresponding authors</p>
  <div class="scholar-row">
    <img src="{{ site.data.site.publications_scholar_image }}" alt="Google Scholar">
  </div>
</section>


<section class="section">
  <div class="section-head">
    <div>
      <p class="eyebrow">HIGHLIGHT</p>
      <h2>RESEARCH OVERVIEW</h2>
    </div>
  </div>
  <div class="image-panel publication-feature-figure">
    <img src="{{ '/assets/images/publication-flowchart.jpg' | relative_url }}" alt="Research overview flowchart">
  </div>
</section>

<section class="section">
  <div class="section-head">
    <div>
      <p class="eyebrow">ARTICLES</p>
      <h2>PUBLICATIONS</h2>
    </div>
  </div>

  <div class="pub-list">
    {% for item in site.data.publications %}
      <article class="pub-item">
        <div class="pub-meta">{{ item.journal }} <span>•</span> {{ item.date }}</div>
        <div class="pub-title">
          {% if item.url == '#' %}
            {{ item.title }}
          {% else %}
            <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>
          {% endif %}
        </div>
        <div>{{ item.authors }}</div>
        {% if item.note %}<div class="note">{{ item.note }}</div>{% endif %}
        {% if item.images %}
          <div class="pub-gallery">
            {% for img in item.images %}
              <img src="{{ img }}" alt="{{ item.title }} figure {{ forloop.index }}">
            {% endfor %}
          </div>
        {% endif %}
      </article>
    {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section-head">
    <div>
      <p class="eyebrow">REVIEWS</p>
      <h2>BOOK CHAPTER &amp; REVIEW</h2>
    </div>
  </div>

  <div class="review-list">
    {% for item in site.data.reviews %}
      <article class="pub-item">
        <div class="pub-meta">{{ item.journal }} <span>•</span> {{ item.date }}</div>
        <div class="pub-title">
          <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>
        </div>
        <div>{{ item.authors }}</div>
        {% if item.note %}<div class="note">{{ item.note }}</div>{% endif %}
      </article>
    {% endfor %}
  </div>
</section>
