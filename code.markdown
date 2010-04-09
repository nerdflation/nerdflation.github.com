---
title: hey self, this is how to write code
layout: default-with-anchors
---

My goal is to be a devastatingly effective software engineer. These notes
summarize the important things that I think I should be learning to that
end. The ideas here are not novel, just useful. They are also incomplete and
possibly wrong, but you've got to start somewhere.

My aim was to condense the most important things I could think of into a mere
ten pages of pithy sayings. That ten-page restriction made more sense when I
wrote these things in LaTeX, not so much now that they're in blog format...

{% for post in site.categories.coding reversed %}
  {% include standard-post.html %}
{% endfor %}

