---
layout: page
title: Authors
permalink: /authorlist/
image: /files/covers/authorpage_cover.jpeg
---
{% assign modigroups = site.authors | group_by: 'order' %}
{% assign priorOrder = "32,33" | split: "," %}

{% for group in modigroups %}
{% if priorOrder contains group.name %}
### {{ group.name }}기
{% assign modiauthors = group.items | sort: 'title' %}
{% for author in modiauthors %}
{% if author.rank %}
* <span style="display: block;width: 60px;height: 60px;margin: 0 auto;border-radius: 100%;background: url({% if author.image %}{{author.image}}{% else %}../assets/images/pc/default_pic_s.png{% endif %}) no-repeat center;background-size: cover;"></span> [{{author.title}} ({{ author.name }}) {{ author.rank }}]({{ site.baseurl }}/authors/{{ author.name }})
{% else %}
* <span style="display: block;width: 60px;height: 60px;margin: 0 auto;border-radius: 100%;background: url({% if author.image %}{{author.image}}{% else %}../assets/images/pc/default_pic_s.png{% endif %}) no-repeat center;background-size: cover;"></span>[{{author.title}} ({{ author.name }})]({{ site.baseurl }}/authors/{{ author.name }})
{% endif %}
{% endfor %}
{% endif %}
{% endfor %}

{% for group in modigroups %}
{% if priorOrder contains group.name %}
{% continue %}
{% endif %}
### {{ group.name }}기
{% assign modiauthors = group.items | sort: 'title' %}
{% for author in modiauthors %}
{% if author.rank %}
* <span style="display: block;width: 60px;height: 60px;margin: 0 auto;border-radius: 100%;background: url({% if author.image %}{{author.image}}{% else %}../assets/images/pc/default_pic_s.png{% endif %}) no-repeat center;background-size: cover;"></span>[{{author.title}} ({{ author.name }}) {{ author.rank }}]({{ site.baseurl }}/authors/{{ author.name }})
{% else %}
* <span style="display: block;width: 60px;height: 60px;margin: 0 auto;border-radius: 100%;background: url({% if author.image %}{{author.image}}{% else %}../assets/images/pc/default_pic_s.png{% endif %}) no-repeat center;background-size: cover;"></span>[{{author.title}} ({{ author.name }})]({{ site.baseurl }}/authors/{{ author.name }})
{% endif %}
{% endfor %}
{% endfor %}