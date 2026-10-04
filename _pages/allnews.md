---
title: "News"
layout: textlay
description: "News from the Multiscale Computational Plasma Lab at UCLA: new papers, invited talks, awards, and lab updates."
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<div style="margin-bottom: 20px;">
  <strong>{{ article.date }}</strong><br>
  {{ article.headline | markdownify | remove: '<p>' | remove: '</p>' }}
</div>
{% endfor %}