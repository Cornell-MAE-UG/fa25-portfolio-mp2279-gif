---
layout: default
title: Michelle Paszek - Portfolio
permalink: https://github.com/Cornell-MAE-UG/fa25-portfolio-mp2279-gif/tree/main/_projects
---

<div class="gallery-container">
<div class="project-gallery">
    {% for project in site.projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" />
          <p>{{ project.title}}</p>
        </a>
      </div>
    {% endfor %}
</div>
</div>
