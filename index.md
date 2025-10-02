---
layout: default
title: Home
---

# Welcome  

Hi, I’m **[Your Name]** 👋  

This is my personal website, built with the Architect theme.  

## 📌 Quick Links
- [About Me](about.md)  
- [Projects](projects.md)  

---

## 🚀 Latest Projects  

<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> – {{ post.date | date: "%B %d, %Y" }}
    </li>
  {% endfor %}
</ul>

[See all projects →](projects.md)
