---
layout: page
title: Projects
permalink: /projects/
---

<div class="card-container">
  {% for project in site.data.projects %}
    <div class="card">
      {% if project.image %}
        <div class="card__background">
            <div class="card__image">
              <img noloading="" width="100%" height="100%" src="{{site.baseurl}}/{{project.image}}" layout="responsive">
            </div>
        </div>
      {% endif %}
      
      <div class="card__content">
        <h4 class="card__title" style="margin-top: 0px;">{{project.name}}</h4>
        <p>{{project.description}}</p>
      </div>
      <div class="card__action">
        {% if project.github %}
          <a href="{{project.github}}">Visit GitHub</a>
        {% endif %}
        {% if project.download %}
          <a href="{{project.download}}">Download</a>
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>
