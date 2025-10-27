---
layout: default
title: Davis Rattanavijai - Portfolio
permalink: /projects/
---

<div class="gallery-container">
<div class="project-gallery">
    {% for project in site.projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <h1>{{ project.title}}</h1>
        </a>
      </div>
    {% endfor %}
</div>
</div>