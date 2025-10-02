---
layout: simple
title: Projects
---

# My Projects  

Here are some of the projects I’ve worked on:

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> – {{ post.date | date: "%B %d, %Y" }}
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>
