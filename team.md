---
layout: default
title: Team
permalink: /team/
---

<style>
.team-profile-block {
  margin: 0 0 28px;
}

.team-profile-head {
  margin: 0 0 20px;
}

.team-profile-head .eyebrow {
  margin: 0;
}

.team-profile-card {
  display: flex;
  align-items: flex-start;
  gap: 36px;
  padding: 8px 0 0;
}

.team-profile-side {
  flex: 0 0 240px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.team-profile-photo {
  width: 118px;
  height: 118px;
  border-radius: 50%;
  overflow: hidden;
  background: #fff;
  margin: 0 0 16px;
}

.team-profile-photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.team-profile-side h3 {
  margin: 0 0 8px;
  font-size: 1rem;
  line-height: 1.32;
  letter-spacing: 0.01em;
  color: var(--ink);
}

.team-profile-role {
  margin: 0 0 6px;
  font-size: 0.86rem;
  line-height: 1.45;
  color: var(--ink);
  font-weight: 600;
}

.team-profile-meta {
  margin: 0;
  font-size: 0.82rem;
  line-height: 1.55;
  color: var(--ink);
}

.team-profile-copy {
  flex: 0 1 760px;
  max-width: 760px;
  min-width: 0;
  padding-top: 2px;
}

.team-profile-bio {
  margin: 0;
  font-size: 1rem;
  line-height: 1.55;
  color: var(--muted);
}

.team-grid--members:empty::before {
  content: "";
  display: block;
  min-height: 12px;
}

.team-section--alumni .member-card .card-body {
  padding-top: 18px;
  padding-bottom: 18px;
}

.team-section--alumni .member-card .card-body h3 {
  margin: 0 0 6px;
  line-height: 1.08;
}

.team-section--alumni .member-card .card-body p,
.team-section--alumni .member-card .member-meta,
.team-section--alumni .member-card .member-link {
  margin: 0 0 2px;
  line-height: 1.08;
}

.team-section--alumni .member-card .card-body p:last-child,
.team-section--alumni .member-card .member-link:last-child {
  margin-bottom: 0;
}

@media (max-width: 980px) {
  .team-profile-card {
    flex-direction: column;
    gap: 26px;
  }

  .team-profile-side {
    flex-basis: auto;
    width: 100%;
  }

  .team-profile-photo {
    width: 118px;
    height: 118px;
  }

  .team-profile-copy {
    max-width: 100%;
    padding-top: 0;
  }
}
</style>

<section class="team-profile-block">
  <div class="team-profile-head">
    <p class="eyebrow">PRINCIPAL INVESTIGATOR</p>
  </div>

  {% assign lead = site.data.team | first %}
  <div class="team-profile-card">
    <div class="team-profile-side">
      <div class="team-profile-photo">
        {% if lead.image contains "://" %}
          <img src="{{ lead.image }}" alt="{{ lead.name }}" loading="lazy">
        {% else %}
          <img src="{{ lead.image | relative_url }}" alt="{{ lead.name }}" loading="lazy">
        {% endif %}
      </div>

      <h3>{{ lead.name }}</h3>
      <p class="team-profile-role">Principal Investigator</p>
      <p class="team-profile-meta">Hainan Medical University</p>
    </div>

    <div class="team-profile-copy">
      <p class="team-profile-bio">Dr. Peng Tan is a professor at Hainan Academy of Medical Sciences, Hainan Medical University. He earned his Ph.D. from Texas A&amp;M University (2018) and conducted off-campus research at Weill Cornell Medical College-Houston campus. He then joined Klarman Cell Observatory, Broad Institute of MIT and Harvard as a postdoctoral associate with professors Aviv Regev and Ramnik Xavier. He was the recipient of Student Research Award and IBD Plexus Award from the Crohn's &amp; Colitis Foundation of America. He has published over 40 publications, including first or corresponding author articles in premier journals (Science, Nature Chemical Biology, Physiological Reviews, Nucleic Acids Research, Molecular Cell, Journal of Clinical Investigation, PLoS Biology, PLoS Pathogens, Oncogene, etc), and contributed significantly to publications in Nature, Nature Medicine, Nature Cell Biology, Cell Host &amp; Microbe, and Immunity, with a total citation of over 4250 and an h-index of 29. His work has been featured or highlighted in multiple media outlets and in journals. As an immuno-oncologist and neuroscientist, Dr. Tan seeks to understand inflammation and disease including cancer across space and time. He investigates how the nervous system mediates long-range organ-organ communications and interacts with the immune system in relation to disease progression. This is achieved through developing and applying interdisciplinary technologies such as proximity-labelling and proteomics, optogenetics, single-cell and spatial multi-omics. He designs molecular perturbations including in vivo Perturb-seq and light-switches to study biological processes and the quantitative consequences at single-cell and systems level.</p>
    </div>
  </div>
</section>

<section class="section team-section team-section--members">
  <div class="section-head">
    <div>
      <p class="eyebrow">LAB MEMBERS</p>
    </div>
  </div>

  <div class="team-grid team-grid--members">
  </div>
</section>

<section class="section team-section team-section--alumni">
  <div class="section-head">
    <div>
      <p class="eyebrow">ALUMNI</p>
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
      <p class="eyebrow">CONSORTIUM</p>
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
