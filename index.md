---
toc: false
---

# HotCarbon -- Workshop on Sustainable Computer Systems

HotCarbon aims to bring together researchers and practitioners in computer and network systems to engage in a lively discussion focused on sustainability throughout the entire lifecycle of modern computing, focusing on both the operational and embodied impact of computer systems.

### Updates and News
<ul class="post-list">
  {% for post in site.posts limit:1 %}
  {% if post.type == "news" %}
  <li>
    <h4>{{ post.title }}
    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span></h4>
    {{ post.content }}
  </li>
  {% endif %}
  {% endfor %}
</ul>