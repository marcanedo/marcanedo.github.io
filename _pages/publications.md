---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

## Submitted Publications

<ol>
{% for post in site.publications %}
  {% if post.status == 'submitted' %}
    <li style="margin-bottom: 10px;">
      {{ post.citation }} 
      {% if post.paperurl %}
        <a href="{{ post.paperurl }}"><strong>[arXiv]</strong></a>
      {% endif %}
    </li>
  {% endif %}
{% endfor %}
</ol>

## Publications in Progress

<ol>
{% for post in site.publications %}
  {% if post.status == 'in progress' %}
    <li style="margin-bottom: 10px;">
      {{ post.citation }}
    </li>
  {% endif %}
{% endfor %}
</ol>