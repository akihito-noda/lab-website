---
layout: default
title: Home
---

<section class="hero">
  <h1>Ubiquitous Imperceptible Electronics Laboratory</h1>
  <p>
    私たちの研究室では、無線通信、ウェアラブルエレクトロニクス、導電布、RFID/UWBセンシング、
    スマート電波環境などを対象に、デバイス開発から通信・計測システム評価まで一体的に研究しています。
  </p>
  <a class="button" href="{{ '/research/' | relative_url }}">研究内容を見る</a>
</section>

## Research Topics

<div class="grid">
{% for item in site.data.research %}
  <section class="card">
    <h3>{{ item.title_ja }}</h3>
    <p>{{ item.description }}</p>
  </section>
{% endfor %}
</div>

## News

<ul class="news-list">
{% for item in site.data.news limit:5 %}
  <li class="news-list-item">

{% if item.image %}
  <div class="news-thumb-wrap">
    {% if item.url and item.url != "" %}
      <a href="{{ item.url }}">
        <img
          src="{{ item.image | relative_url }}"
          alt="{{ item.image_alt | default: item.title }}"
          class="news-thumb">
      </a>
    {% else %}
      <img
        src="{{ item.image | relative_url }}"
        alt="{{ item.image_alt | default: item.title }}"
        class="news-thumb">
    {% endif %}
  </div>
{% endif %}

<div class="news-list-text">
  <div class="meta">{{ item.date }}</div>

  {% if item.url and item.url != "" %}
    <a href="{{ item.url }}">{{ item.title }}</a>
  {% else %}
    {{ item.title }}
  {% endif %}
</div>

  </li>
{% endfor %}
</ul>

<p class="news-more">
  <a href="{{ '/news/' | relative_url }}">View all news →</a>
</p>


## For Prospective Students

本研究室では、実際に動作するハードウェア・システムを作りあげ、評価し、論文として説明できる形にまとめることを重視しています。
研究室配属を希望する学生は、[配属希望者向けページ]({{ '/for-students/' | relative_url }})も確認してください。
