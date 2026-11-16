---
layout: page
title: Projects
permalink: /projects/
description: Laboratory and design projects in digital design, analog and RF circuits, embedded systems, and signal processing. Click a project to open its files on Google Drive.
nav: true
nav_order: 4
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
  {% assign sorted_all = site.projects | sort: "importance" %}
  {% for category in site.data.project_categories %}
    {% assign group = sorted_all | where: "category", category %}
    {% if group.size > 0 %}
      <h2 class="category" id="{{ category | slugify }}">{{ category }}</h2>
      <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3">
        {% for project in group %}
          {% include projects.liquid %}
        {% endfor %}
      </div>
    {% endif %}
  {% endfor %}
</div>
