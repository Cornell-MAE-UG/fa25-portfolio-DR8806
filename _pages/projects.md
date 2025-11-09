---
layout: default
title: Davis Rattanavijai - Portfolio
permalink: /projects/
---

<div class="gallery-container">
  <div class="project-gallery">

    <!-- Math Modeling Papers -->
    <h2 class="text-center mb-4">Math Modeling Papers</h2>
    {% assign math_projects = site.projects | where: "category", "Math Model Papers" | sort: "order" %}
    {% for project in math_projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <h3>{{ project.title }}</h3>
        </a>
      </div>
    {% endfor %}

    <!-- Cornell FSAE -->
    <h2 class="text-center mb-4 mt-5">Cornell FSAE</h2>
    {% assign cornell_projects = site.projects | where: "category", "Cornell FSAE" | sort: "order" %}
    {% for project in cornell_projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <h3>{{ project.title }}</h3>
        </a>
      </div>
    {% endfor %}

    <!-- Personal Projects -->
    <h2 class="text-center mb-4 mt-5">Personal Projects</h2>
    {% assign personal_projects = site.projects | where: "category", "Personal Projects" | sort: "order" %}
    {% for project in personal_projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <h3>{{ project.title }}</h3>
        </a>
      </div>
    {% endfor %}

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