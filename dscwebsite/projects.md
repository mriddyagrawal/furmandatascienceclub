---
layout: page
title: "Projects"
permalink: /projects/
---

<!-- Link to the projects.css -->
<link rel="stylesheet" href="{{ '/assets/css/projects.css' | relative_url }}">

# Data Science Projects at Furman

Welcome to the Data Science projects page. Here you can find some of the exciting projects from various Data Science classes at Furman University.

<div class="projects-grid">
  {% for post in site.posts %}
    {% if post.categories contains "Data Science" %}
      <div class="project-card">
        <div class="project-thumbnail">
          <img src="{{ post.thumbnail | relative_url }}" alt="{{ post.title }} thumbnail">
        </div>
        <div class="project-details">
          <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
          <p><strong>{{ post.date | date: "%Y" }}</strong></p>
          <p>{{ post.excerpt | truncatewords: 20 }}</p>
          <a href="{{ post.url }}" class="read-more">Read more</a>
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>

