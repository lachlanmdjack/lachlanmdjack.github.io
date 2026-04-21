---
layout: default
---

<link rel="stylesheet" href="{{ '/assets/css/style.css' | relative_url }}">

<header class="ringer-header">
  <h1>HOLIDAY PHOTO DRAFT</h1>
  <p>2024 SEASON RECAP</p>
</header>

<div class="draft-container">
  {% for photo in site.photos %}
  <div class="photo-card">
    <div class="photo-header">
      <span class="location">{{ photo.location }}</span>
      <span class="rank">{{ photo.rank }}</span>
    </div>
    
    <div class="img-container">
      <img src="{{ photo.image_path | relative_url }}" alt="{{ photo.title }}">
    </div>

    <div class="photo-info">
      <h3>{{ photo.title }}</h3>
      <p>{{ photo.content | strip_html }}</p>
      <div class="tags">
        {% for tag in photo.tags %}
          <span class="tag">#{{ tag }}</span>
        {% endfor %}
      </div>
    </div>
  </div>
  {% endfor %}
</div>