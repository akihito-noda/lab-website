---
layout: default
title: Publications
permalink: /publications/
---

# Publications
<!--
業績一覧は `_data/publications.yml` を編集すると更新できます。
-->
{% assign pubs_by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}
{% for year in pubs_by_year %}
## {{ year.name }}

<ul class="publication-list">
{% for p in year.items %}
  <li>
    <span class="tag">{{ p.type }}</span>
    <strong>{{ p.title }}</strong><br>
    {{ p.authors }}<br>
    <em>{{ p.venue }}</em>{% if p.status %}, {{ p.status }}{% endif %}.
    {% if p.url != "" %}<br><a href="{{ p.url }}">Link</a>{% endif %}
  </li>
{% endfor %}
</ul>
{% endfor %}
