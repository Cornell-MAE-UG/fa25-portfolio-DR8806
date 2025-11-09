---
layout: default
title: Davis Rattanavijai - Portfolio
permalink: /projects/
---

<div class="gallery-container">

  <!-- Math Modeling Papers -->
  <div class="category-block math-block">
    <h2 class="category-title">Math Modeling Papers</h2>
    <div class="project-gallery">
      {% assign math_projects = site.projects | where: "category", "Math Model Papers" | sort: "order" %}
      {% for project in math_projects %}
        <div class="gallery-item">
          <a href="{{ project.url | relative_url }}">
            <h3>{{ project.title }}</h3>
          </a>
        </div>
      {% endfor %}
    </div>
  </div>

  <!-- Cornell FSAE -->
  <div class="category-block fsae-block">
    <h2 class="category-title">Cornell FSAE</h2>
    <div class="project-gallery">
      {% assign cornell_projects = site.projects | where: "category", "Cornell FSAE" | sort: "order" %}
      {% for project in cornell_projects %}
        <div class="gallery-item">
          <a href="{{ project.url | relative_url }}">
            <h3>{{ project.title }}</h3>
          </a>
        </div>
      {% endfor %}
    </div>
  </div>

  <!-- Personal Projects -->
  <div class="category-block personal-block">
    <h2 class="category-title">Personal Projects</h2>
    <div class="project-gallery">
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