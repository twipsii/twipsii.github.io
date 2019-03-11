---
layout: default
title: This is my blog
---

{% for post in site.posts %}
  {% include post_excerpt.html %}
{% endfor %}