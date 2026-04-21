---
layout: archive
title: "Notes"
permalink: /notes/
author_profile: true
---

{% for post in site.posts %}
  {% if post.categories contains 'notes' %}
  <div style="margin-bottom: 1.5em;">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p style="color: #666; font-size: 0.85em;">{{ post.date | date: "%B %d, %Y" }}</p>
    {% if post.excerpt %}
    <p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
    {% endif %}
  </div>
  {% endif %}
{% endfor %}