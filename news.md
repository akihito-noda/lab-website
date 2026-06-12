---
layout: default
title: News
permalink: /news/
---

# News

<ul class="news-list">
{% for item in site.data.news %}
  <li>
    <div class="meta">{{ item.date }}</div>
    {% if item.url != "" %}
      <a href="{{ item.url }}">{{ item.title }}</a>
    {% else %}
      {{ item.title }}
    {% endif %}
  </li>
{% endfor %}
</ul>
