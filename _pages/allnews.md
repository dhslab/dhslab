---
title: "News"
layout: textlay
excerpt: "Spencer Lab at Washington University in St. Louis School of Medicine."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br>
<em>{{ article.headline | markdownify}}</em></p>
{% endfor %}
