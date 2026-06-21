---
layout: default
title: Research
permalink: /research/
---

# Research

本研究室では、無線通信技術と高周波電子回路技術を基盤として、身体・衣服・室内空間に広がる新しい通信・センシングシステムを研究しています。

{% for item in site.data.research %}

<section class="research-section" markdown="1">

## {{ item.title_ja }}

{% if item.title %}
**{{ item.title }}**
{% endif %}

{% if item.video %} <video
class="research-page-media"
autoplay
muted
loop
playsinline
preload="metadata"
aria-label="{{ item.title_ja }}の研究紹介動画"> <source src="{{ item.video | relative_url }}" type="video/mp4">
お使いのブラウザは動画表示に対応していません。 </video>
{% elsif item.image %} <img
src="{{ item.image | relative_url }}"
alt="{{ item.image_alt | default: item.title_ja }}"
class="research-page-media">
{% endif %}

{{ item.description }}

</section>
{% endfor %}


<!--
## 研究の進め方

単に理論モデルを検討するだけでなく、回路・基板・アンテナ・センサ・ソフトウェアを実装し、実測評価を通じてシステムとしての有効性を検証します。
-->
