---
title: Portfolio
layout: collection
permalink: /portfolio/
collection: portfolio
entries_layout: grid
classes: wide
autor profile: true
---

Professional and personal art projects.

{% assign sorted = site.resources | reverse %}
{% for item in sorted %}
  <h1>{{ item.name }}</h1>
  <p>{{ item.content }}</p>
{% endfor %}