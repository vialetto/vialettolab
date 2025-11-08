---
title: "News"
layout: textlay
excerpt: "Multiscale Computational Plasma Lab at UCLA"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<div style="margin-bottom: 20px;">
  <strong>{{ article.date }}</strong><br>
  {{ article.headline | markdownify | remove: '<p>' | remove: '</p>' }}
</div>
{% endfor %}