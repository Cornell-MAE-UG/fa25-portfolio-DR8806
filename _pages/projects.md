---
layout: default
title: Davis Rattanavijai - Portfolio
permalink: /projects/
---

<div class="projects-container">

  <div class="category-section math-section">
    <h2>Math Modeling</h2>
    <ul class="project-list">
      {% assign math_projects = site.projects | where: "category", "Math Model Papers" | sort: "order" %}
      {% for project in math_projects %}
        <li><a href="{{ project.url | relative_url }}">{{ project.title }}</a></li>
      {% endfor %}
    </ul>
  </div>

  <div class="category-section fsae-section">
    <h2>Cornell FSAE</h2>
    <ul class="project-list">
      {% assign cornell_projects = site.projects | where: "category", "Cornell FSAE" | sort: "order" %}
      {% for project in cornell_projects %}
        <li><a href="{{ project.url | relative_url }}">{{ project.title }}</a></li>
      {% endfor %}
    </ul>
  </div>

  <div class="category-section personal-section">
    <h2>Personal Projects</h2>
    <ul class="project-list">
      {% assign personal_projects = site.projects | where: "category", "Personal Projects" | sort: "order" %}
      {% for project in personal_projects %}
        <li><a href="{{ project.url | relative_url }}">{{ project.title }}</a></li>
      {% endfor %}
    </ul>
  </div>

</div>




<!--
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
          <h3>{{ project.title}}</h3>
        </a>
      </div>
    {% endfor %}
</div>
</div>

-->