---
layout: default
comments: true
---
<a href="#" onclick="history.go(-1)">← Go Back</a>
<h2 class="post_title">
  {{ page.title }}
</h2>
<!--<p>
{% if page.date %}
    <small>{{ page.date | date_to_string }}</small>
{% endif %}
</p>-->

{{ content }}