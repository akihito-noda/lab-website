---
layout: default
title: Members
permalink: /members/
---

# Members

## Faculty

<ul class="member-list">
{% for m in site.data.members %}
{% if m.group == "faculty" %}
  <li>
    <strong>{{ m.name }}</strong>{% if m.name_en %} / {{ m.name_en }}{% endif %}<br>
    <span class="meta">{{ m.role }}</span><br>
    {% if m.email %}<span class="meta">Email: {{ m.email }}</span><br>{% endif %}
    {% for tag in m.interests %}<span class="tag">{{ tag }}</span>{% endfor %}
  </li>
{% endif %}
{% endfor %}
</ul>

## Students

<ul class="member-list">
{% for m in site.data.members %}
{% if m.group == "students" %}
  <li>
    <strong>{{ m.name }}</strong><br>
    <span class="meta">{{ m.role }}</span><br>
    {% for tag in m.interests %}<span class="tag">{{ tag }}</span>{% endfor %}
  </li>
{% endif %}
{% endfor %}
</ul>

## Alumni

<ul class="member-list">
{% for m in site.data.members %}
{% if m.group == "alumni" %}
  <li>
    <strong>{{ m.name }}</strong><br>
    <span class="meta">{{ m.role }}{% if m.year %}, {{ m.year }}{% endif %}</span>
  </li>
{% endif %}
{% endfor %}
</ul>
