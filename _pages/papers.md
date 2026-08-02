---
layout: page
title: papers
permalink: /papers/
nav: false
description: Papers I am reading, have read, or want to revisit.
---

<div class="papers-intro">
  A running log of papers I find interesting.
</div>

{% assign papers = site.data.papers %}

{% if papers and papers.size > 0 %}
<div class="papers-list">
  {% for paper in papers %}
  <div class="paper-card">
    <div class="paper-card-top">
      {% if paper.venue %}
      <span class="paper-venue">{{ paper.venue }}</span>
      {% endif %}
      {% if paper.status %}
      <span class="paper-status-badge status-{{ paper.status | slugify }}">{{ paper.status }}</span>
      {% endif %}
    </div>
    <h3 class="paper-title">
      {% if paper.url %}
      <a href="{{ paper.url }}" target="_blank" rel="noopener noreferrer">{{ paper.title }}</a>
      {% else %}
      {{ paper.title }}
      {% endif %}
    </h3>
    {% if paper.authors %}
    <p class="paper-authors">{{ paper.authors }}</p>
    {% endif %}
    {% if paper.notes %}
    <details class="paper-notes-toggle">
      <summary>Notes</summary>
      <ul>
        {% for note in paper.notes %}
        <li>{{ note }}</li>
        {% endfor %}
      </ul>
    </details>
    {% endif %}
  </div>
  {% endfor %}
</div>
{% else %}
<p class="papers-empty">Papers coming soon.</p>
{% endif %}
