---
layout: default
title: Members
permalink: /members/
---

# Members

## Faculty

<ul class="member-list">
{% for m in site.data.members.faculty %}
  <li>
    <strong>{% if m.url %}<a href="{{ m.url }}">{{ m.name }}</a>{% else %}{{ m.name }}{% endif %}</strong>{% if m.name_en %} / {{ m.name_en }}{% endif %}<br>
    <span class="meta">{{ m.role }}</span><br>
    {% if m.email %}<span class="meta">Email: {{ m.email }}</span><br>{% endif %}
    {% for tag in m.interests %}<span class="tag">{{ tag }}</span>{% endfor %}
  </li>
{% endfor %}
</ul>

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
