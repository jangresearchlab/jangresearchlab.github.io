---
layout: page
title: Research
permalink: /projects/
nav: true
nav_order: 2
---

<div class="projects-scroll">
  {% assign projects = site.data.projects %}
  {% for proj in projects %}
    <div class="project-item">
      {% if proj.image %}
        <img
          class="project-thumb"
          src="{{ '/assets/img/' | append: proj.image | relative_url }}"
          alt="{{ proj.title }}"
        >
      {% endif %}

      <div class="project-text">
        {% if proj.link %}
          <h3 class="project-title">
            <a href="{{ proj.link | relative_url }}">{{ proj.title }}</a>
          </h3>
        {% else %}
          <h3 class="project-title">{{ proj.title }}</h3>
        {% endif %}

        <p class="project-desc">
        {{ proj.description | markdownify }}
        </p>
      </div>
    </div>
  {% endfor %}
</div>

