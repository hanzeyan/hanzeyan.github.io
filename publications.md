---
layout: default
title: Publications
permalink: /publications/
---

<section class="page-hero page-hero--compact">
  <p class="eyebrow">PUBLICATIONS</p>
  <p># denotes co-first authors; * denotes corresponding authors</p>
  <div class="scholar-row">
    <a href="https://scholar.google.com/citations?user=i6kV0H8AAAAJ&hl=en&oi=ao" target="_blank" rel="noopener noreferrer">
      <img src="{{ site.data.site.publications_scholar_image }}" alt="Google Scholar">
    </a>
  </div>
</section>

<section class="section">
  <div class="section-head">
    <div>
      <p class="eyebrow">HIGHLIGHT</p>
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
    </div>
  </div>

  <div class="pub-list">
    {% for item in site.data.publications %}
      <article class="pub-item">
        <div class="pub-meta">
          <span class="pub-journal">{{ item.journal }}</span>
          <span>•</span>
          <span class="pub-date">{{ item.date }}</span>
        </div>
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
              <img src="{{ img | relative_url }}" alt="{{ item.title }} figure {{ forloop.index }}">
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
    </div>
  </div>

  <div class="review-list">
    {% for item in site.data.reviews %}
      <article class="pub-item">
        <div class="pub-meta">
          <span class="pub-journal">{{ item.journal }}</span>
          <span>•</span>
          <span class="pub-date">{{ item.date }}</span>
        </div>
        <div class="pub-title">
          <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>
        </div>
        <div>{{ item.authors }}</div>
        {% if item.note %}<div class="note">{{ item.note }}</div>{% endif %}
        {% if item.images %}
          <div class="pub-gallery">
            {% for img in item.images %}
              <img src="{{ img | relative_url }}" alt="{{ item.title }} figure {{ forloop.index }}">
            {% endfor %}
          </div>
        {% endif %}
      </article>
    {% endfor %}
  </div>
</section>
