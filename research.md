---
layout: default
title: Research
permalink: /research/
---

# Research

本研究室では、無線通信技術と高周波電子回路技術を基盤として、身体・衣服・室内空間に広がる新しい通信・センシングシステムを研究しています。

{% for item in site.data.research %}
## {{ item.title_ja }}

**{{ item.title }}**

{{ item.description }}

{% endfor %}

<--
## 研究の進め方

単に理論モデルを検討するだけでなく、回路・基板・アンテナ・センサ・ソフトウェアを実装し、実測評価を通じてシステムとしての有効性を検証します。
-->
