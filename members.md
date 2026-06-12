---
layout: default
title: Members
permalink: /members/
---

# Members

## Faculty

{% for person in site.data.members.faculty %}
<div class="member-card">
  <h3>
    {% if person.profile_url %}
      <a href="{{ person.profile_url }}" target="_blank" rel="noopener">
        {{ person.name }}
      </a>
    {% else %}
      {{ person.name }}
    {% endif %}
  </h3>

  {% if person.name_en %}
  <p class="muted">{{ person.name_en }}</p>
  {% endif %}

  {% if person.role %}
  <p>{{ person.role }}</p>
  {% endif %}

  {% if person.email %}
  <p>Email: {{ person.email }}</p>
  {% endif %}

  {% if person.interests %}
  <p>
    Research interests:
    {{ person.interests | join: " / " }}
  </p>
  {% endif %}
</div>
{% endfor %}

## Students
<!-- 
<p>学生については、個人名を掲載せず、課程・学年ごとの人数のみを掲載しています。</p>
-->

<table class="member-table">
  <thead>
    <tr>
      <th>課程</th>
      <th>学年</th>
      <th>人数</th>
    </tr>
  </thead>
  <tbody>
{% for group in site.data.members.students %}
{% for grade in group.grades %}
{% if grade.count and grade.count > 0 %}
    <tr>
      <td>{{ group.degree }}</td>
      <td>{{ grade.year }}</td>
      <td>{{ grade.count }}名</td>
    </tr>
{% endif %}
{% endfor %}
{% endfor %}
  </tbody>
</table>
<p>※学士課程については今年度卒業研究を履修している人数を掲載しています。</p>

## Alumni
<!-- 
<p>卒業生についても、個人名ではなく、年度ごとの修了・卒業人数を掲載しています。</p>
-->

<table class="member-table">
  <thead>
    <tr>
      <th>年度</th>
      <th>課程</th>
      <th>人数</th>
    </tr>
  </thead>
  <tbody>
{% for year in site.data.members.alumni %}
{% for item in year.counts %}
{% if item.count and item.count > 0 %}
    <tr>
      <td>{{ year.fiscal_year }}年度</td>
      <td>{{ item.degree }}</td>
      <td>{{ item.count }}名</td>
    </tr>
{% endif %}
{% endfor %}
{% endfor %}
  </tbody>
</table>
