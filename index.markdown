---
layout: default
---

{% for post in site.posts limit:5 %}
  {% include standard-post.html %}
{% endfor %}

<table id="footer-links">
  <tr>
    <td>
    </td>
    <td id="older-posts">
      <a href="/archive.html">All posts</a> &rarr;
    </td>
</tr>
</table>
