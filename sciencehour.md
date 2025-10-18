---
layout: default
title: "Science Hour Club"
---

[Home](index.md)

<h1>Science Hour Club Events</h1>

{% for event in site.sciencehour reversed %}
  <h3><a href="{{ event.url | relative_url }}">{{ event.title }}</a></h3>
  <p>{{ event.date | date: "%B %d, %Y" }}</p>
  <hr>
{% endfor %}
