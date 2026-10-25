---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<style>
  /* Estilos para imitar el formato del CV en LaTeX */
  .cv-list {
    padding-left: 1.5em;
    margin-bottom: 2em;
  }
  .cv-list li {
    margin-bottom: 0.8em; /* Espaciado compacto pero legible */
    line-height: 1.4;
  }
  .cv-link {
    color: inherit; 
    text-decoration: none; 
    border-bottom: none;
  }
  .cv-link:hover {
    text-decoration: underline; 
  }
  
  /* El equivalente a \hfill en web */
  .cv-details {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
  }
  .cv-citation {
    padding-right: 1em; /* Da un respiro si la cita es muy larga */
  }
  .cv-badge {
    white-space: nowrap; /* Mantiene el [arXiv] en una sola pieza */
  }
</style>

{% if author.googlescholar %}
  <p style="font-size: 0.9em;">You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a></u>.</p>
{% endif %}

## Submitted Publications

<ol reversed class="cv-list">
{% for post in site.publications reversed %}
  {% if post.status == 'submitted' %}
    <li>
      <div class="cv-details">
        <span class="cv-citation">
          <!-- Si quieres que el clic vaya a tu pgina interna, puedes envolver post.citation as:
          <a href="{{ base_path }}{{ post.url }}" class="cv-link">{{ post.citation }}</a> -->
          {{ post.citation }}
        </span>
        {% if post.paperurl %}
          <span class="cv-badge">
            <a href="{{ post.paperurl }}" class="cv-link"><strong>[arXiv]</strong></a>
          </span>
        {% endif %}
      </div>
    </li>
  {% endif %}
{% endfor %}
</ol>

## Publications in Progress

<ol reversed class="cv-list">
{% for post in site.publications reversed %}
  {% if post.status == 'in progress' %}
    <li>
      <div class="cv-details">
        <span class="cv-citation">{{ post.citation }}</span>
      </div>
    </li>
  {% endif %}
{% endfor %}
</ol>