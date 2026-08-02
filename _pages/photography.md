---
layout: page
permalink: /photography/
title: photography
nav: false
description: Things I noticed. Places I've been. Moments worth keeping.
---

<!-- <div class="photo-intro">
  I don't always have time to write. Sometimes a frame says it better anyway.
</div> -->

{% assign all_photos = site.photography %}
{% assign categories = all_photos | map: 'category' | uniq %}

{% if all_photos.size > 0 %}
  <div class="photo-filter-bar">
    <button class="photo-filter-btn active" data-filter="all" onclick="filterPhotos(this, 'all')">All</button>
    {% for cat in categories %}
      <button class="photo-filter-btn" data-filter="{{ cat }}" onclick="filterPhotos(this, '{{ cat }}')">{{ cat | capitalize }}</button>
    {% endfor %}
  </div>

  <div class="photo-grid" id="photo-grid">
    {% for photo in all_photos %}
    <div class="photo-item" data-category="{{ photo.category }}">
      <div class="photo-inner">
        <img
          src="{{ photo.img | relative_url }}"
          alt="{{ photo.caption }}"
          loading="lazy"
          class="photo-img"
        />
        <div class="photo-overlay">
          <p class="photo-caption">{{ photo.caption }}</p>
          {% if photo.location %}
            <span class="photo-location">
              <i class="fa-solid fa-location-dot"></i> {{ photo.location }}
            </span>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>

  <script>
    function filterPhotos(btn, filter) {
      document.querySelectorAll('.photo-filter-btn').forEach(function(b) {
        b.classList.remove('active');
      });
      btn.classList.add('active');

      document.querySelectorAll('.photo-item').forEach(function(item) {
        if (filter === 'all' || item.getAttribute('data-category') === filter) {
          item.style.display = '';
        } else {
          item.style.display = 'none';
        }
      });
    }
  </script>
{% else %}
  <p class="photo-empty">Photos coming soon.</p>
{% endif %}
