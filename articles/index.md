---
title: Articles
layout: page
permalink: /articles/
---

## Topics
<ul>
{%- assign groups = site.articles
  | group_by_exp: "d", "d.path | split: '/' | slice: 1, 1 | first | default: 'misc'"
  | sort: "name" -%}
{%- for g in groups -%}
  <li>
    <a href="{{ '/' | append: g.name | append: '/' | relative_url }}"><strong>{{ g.name }}/</strong></a>
    <small>({{ g.items | size }})</small>
  </li>
{%- endfor -%}
</ul>

