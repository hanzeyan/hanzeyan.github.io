---
layout: default
title: Team
permalink: /team/
---

<section class="page-hero page-hero--compact team-page-hero">
  <p class="eyebrow">TEAM</p>
  <h1>LAB MEMBERS</h1>
  <p>Our team works across computational biology, single-cell and spatial multi-omics, immunology, neuroscience, microbiology, protein engineering and synthetic biology.</p>
</section>

<section class="section team-section team-section--current">
  <div class="section-head">
    <div>
      <p class="eyebrow">TEAM</p>
      <h2>Principal Investigator</h2>
    </div>
  </div>

  {% assign lead = site.data.team | first %}
  <div class="team-grid team-grid--pi">
    <article class="member-card member-card--lead">
      <div class="member-avatar">
        {% if lead.image contains "://" %}
          <img src="{{ lead.image }}" alt="{{ lead.name }}" loading="lazy">
        {% else %}
          <img src="{{ lead.image | relative_url }}" alt="{{ lead.name }}" loading="lazy">
        {% endif %}
      </div>
      <div class="card-body">
        <h3>{{ lead.name }}</h3>
        <p class="member-meta">{{ lead.role }}</p>
        {% for line in lead.lines %}
          <p>{{ line }}</p>
        {% endfor %}
        {% if lead.link %}
          <p class="member-link">
            <a href="{{ lead.link }}" target="_blank" rel="noopener noreferrer">{{ lead.link }}</a>
          </p>
        {% endif %}
      </div>
    </article>
  </div>
</section>

<section class="section team-section team-section--members">
  <div class="section-head">
    <div>
      <p class="eyebrow">TEAM</p>
      <h2>Lab Members</h2>
    </div>
  </div>

  <div class="team-grid team-grid--members">
    {% for member in site.data.team offset:1 %}
      <article class="member-card">
        <div class="member-avatar">
          {% if member.image contains "://" %}
            <img src="{{ member.image }}" alt="{{ member.name }}" loading="lazy">
          {% else %}
            <img src="{{ member.image | relative_url }}" alt="{{ member.name }}" loading="lazy">
          {% endif %}
        </div>
        <div class="card-body">
          <h3>{{ member.name }}</h3>
          <p class="member-meta">{{ member.role }}</p>
          {% for line in member.lines %}
            <p>{{ line }}</p>
          {% endfor %}
          {% if member.link %}
            <p class="member-link">
              <a href="{{ member.link }}" target="_blank" rel="noopener noreferrer">{{ member.link }}</a>
            </p>
          {% endif %}
        </div>
      </article>
    {% endfor %}
  </div>
</section>

<section class="section team-section">
  <div class="section-head">
    <div>
      <p class="eyebrow">AFFILIATION</p>
      <h2>Affiliation</h2>
    </div>
  </div>
  <div class="logo-grid">
    {% for item in site.data.affiliations %}
      <div class="logo-card">
        {% if item.image contains "://" %}
          <img src="{{ item.image }}" alt="{{ item.title }}">
        {% else %}
          <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
        {% endif %}
      </div>
    {% endfor %}
  </div>
</section>

<section class="section team-section">
  <div class="section-head">
    <div>
      <p class="eyebrow">CONSORTIUM</p>
      <h2>Consortium</h2>
    </div>
  </div>
  <div class="logo-grid">
    {% for item in site.data.consortium %}
      <div class="logo-card">
        {% if item.image contains "://" %}
          <img src="{{ item.image }}" alt="{{ item.title }}">
        {% else %}
          <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
        {% endif %}
      </div>
    {% endfor %}
  </div>
</section>
