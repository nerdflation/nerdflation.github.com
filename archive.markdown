---
layout: default
title: post archive
---

{% for post in site.posts %}
  {% include standard-post.html %}
{% endfor %}
