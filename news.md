---
layout: default
title: News
permalink: /news/
---

# News

<ul class="news-list">
{% for item in site.data.news %}
  <li class="news-item">

<div class="meta">{{ item.date }}</div>

<div class="news-title">
  {% if item.url and item.url != "" %}
    <a href="{{ item.url }}">{{ item.title }}</a>
  {% else %}
    {{ item.title }}
  {% endif %}
</div>

{% if item.image %}
  {% if item.url and item.url != "" %}
    <a href="{{ item.url }}">
      <img
        src="{{ item.image | relative_url }}"
        alt="{{ item.image_alt | default: item.title }}"
        class="news-image">
    </a>
  {% else %}
    <img
      src="{{ item.image | relative_url }}"
      alt="{{ item.image_alt | default: item.title }}"
      class="news-image">
  {% endif %}
{% endif %}

{% if item.description %}
  <div class="news-description">
    {{ item.description }}
  </div>
{% endif %}

  </li>
{% endfor %}
</ul>
