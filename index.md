---
layout: default
title: Home
---

# Welcome  

Hi, I’m **Ivan Johnson** 

This is my personal website.  

##  Quick Links
- [About Me](about.md)  

---

## Science Hour
- [Science Hour Club](sciencehour.md)

---

##  Latest Projects  

<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> – {{ post.date | date: "%B %d, %Y" }}
    </li>
  {% endfor %}
</ul>


### [Anscombe’s Quartet – Data Visualization Blog](posts/anscombe-eda/)
An in-depth analysis of how identical statistics can create visually different datasets.

