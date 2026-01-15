---
layout: default
title: Blog
nav_order: 10
---

# TrackMe+ Blog

Tips, guides, and insights for optimizing your health tracking.

---

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %d, %Y" }}* {% if post.author %}| By {{ post.author }}{% endif %}

{{ post.excerpt }}

[Read more →]({{ post.url | relative_url }})

---

{% endfor %}

{% if site.posts.size == 0 %}
*New articles coming soon! Check back for tips on peptide tracking, dosing calculators, and health optimization.*
{% endif %}
