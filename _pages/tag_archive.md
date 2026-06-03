---
title: "Tags"
permalink: /tags/
layout: tags
author_profile: true
---

{% assign docs_by_tags = site.documents | group_by: 'tags' %}
{% for tag in docs_by_tags %}
<h2>{{ tag.name }}</h2>
<ul>
    {% for item in tag.items %}
    <li><a href="{{ item.url }}">{{ item.title }}</a></li>
    {% endfor %}
</ul>
{% endfor %}