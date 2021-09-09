---
layout: page
title: Authors
permalink: /authorlist/
sitemap:
  priority: 0.7
---
{% assign modiauthors = site.authors | sort:'title' %}
{% for author in modiauthors %}
* [{{author.title}} ({{ author.name }})]({{ site.baseurl }}/authors/{{ author.name }})
{% endfor %}
