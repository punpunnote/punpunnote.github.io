---
layout: page
title: カテゴリ一覧
permalink: /categories/
---

{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
## {{ category[0] }}

{% for post in category[1] %}
- [{{ post.title }}]({{ post.url | relative_url }})
{%- endfor %}

{% endfor %}
