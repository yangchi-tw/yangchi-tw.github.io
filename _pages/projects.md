---
permalink: /projects/
title: "Projects"
layout: single
author_profile: true
classes: wide
---

Welcome to my portfolio! Here you'll find a selection of projects that showcase my skills and experience in software development, from web applications to game development.

<div class="feature__wrapper">
{% for project in site.projects %}
  <div class="feature__item">
    <div class="archive__item">
      {% if project.header.teaser %}
        <div class="archive__item-teaser">
          <img src="{{ project.header.teaser | relative_url }}" alt="{{ project.title }}">
        </div>
      {% endif %}
      <div class="archive__item-body">
        <h2 class="archive__item-title">
          <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
        </h2>
        {% if project.excerpt %}
          <div class="archive__item-excerpt">
            {{ project.excerpt | markdownify }}
          </div>
        {% endif %}
        <p><a href="{{ project.url | relative_url }}" class="btn btn--primary">View Project</a></p>
      </div>
    </div>
  </div>
{% endfor %}
</div>

---

*For more projects and code samples, visit my [GitHub profile](https://github.com/Chenade).*