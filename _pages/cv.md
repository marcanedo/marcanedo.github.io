---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<style>
  /* Tipografía y espaciado general del CV */
  .cv-section {
    margin-bottom: 2.5em;
  }
  .cv-section h2 {
    border-bottom: 2px solid #ddd;
    padding-bottom: 0.2em;
    margin-top: 1.5em;
    margin-bottom: 1em;
    font-size: 1.5em;
  }
  
  /* Contenedores para emular \hfill */
  .cv-item {
    margin-bottom: 1.2em;
  }
  .cv-details {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    margin-bottom: 0.2em;
  }
  .cv-left {
    padding-right: 1em; 
  }
  .cv-right {
    white-space: nowrap; 
    font-variant-numeric: tabular-nums; 
    font-weight: 500;
  }
  
  /* Sub-listas (para tutores, tesis, etc) */
  .cv-sublist {
    margin-top: 0;
    margin-bottom: 0;
    padding-left: 1.5em;
    list-style-type: disc;
    font-size: 0.95em;
  }
  
  /* Listas ordenadas para publicaciones y charlas */
  .cv-enum {
    padding-left: 1.5em;
    margin-bottom: 1em;
  }
  .cv-enum li {
    margin-bottom: 0.8em;
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
</style>

<div style="float: right; margin-top: -4em; position: relative; z-index: 10;">
  <a href="https://github.com/marcanedo/cv/blob/master/MarCanedo.pdf?raw=true" class="btn btn--primary">
    <i class="fas fa-file-pdf"></i> Download CV (PDF)
  </a>
</div>
<div style="clear: both;"></div>

<div class="cv-section">
  <h2>Employment</h2>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>Postdoctoral Researcher</strong>, <em>Instituto de Matemática Pura e Aplicada (IMPA)</em>. Rio de Janeiro, Brazil.</span>
      <span class="cv-right">Oct 2026 &ndash; Present</span>
    </div>
  </div>
</div>

<div class="cv-section">
  <h2>Education</h2>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>Ph.D., Mathematics</strong>, <em>Pontificia Universidad Católica de Chile</em>. Santiago, Chile.</span>
      <span class="cv-right">Sep 2026</span>
    </div>
    <ul class="cv-sublist">
      <li>Dissertation Advisor: Prof. Giancarlo Urzúa.</li>
      <li>Dissertation Title: On Surfaces with ℚHD singularities.</li>
    </ul>
  </div>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>M.Sc., Mathematics</strong>, <em>Pontificia Universidad Católica de Chile</em>. Santiago, Chile.</span>
      <span class="cv-right">Jan 2024</span>
    </div>
  </div>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>B.S., Mathematics</strong>, <em>Universidad Mayor de San Andrés</em>. La Paz, Bolivia.</span>
      <span class="cv-right">June 2021</span>
    </div>
    <ul class="cv-sublist">
      <li>Degree conferred with highest honors.</li>
    </ul>
  </div>
</div>

<div class="cv-section">
  <h2>Research Interests</h2>
  <p style="text-align: justify; margin-top: -0.5em;">
    My research lies in the intersection of birational geometry and deformation theory of algebraic projective surfaces over the complex numbers. I have worked on the construction of ℚ-Gorenstein smoothings of singular algebraic projective surfaces, with particular interest in degenerations that preserve the Betti numbers and their applications into problems of algebraic geometry.
  </p>
</div>

<div class="cv-section">
  <h2>Honors and Awards</h2>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>ANID Doctoral Fellowship</strong>, <em>Agencia Nacional de Investigación y Desarrollo, Chile</em></span>
      <span class="cv-right">2022 &ndash; 2026</span>
    </div>
  </div>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>ANID Operational Research Grant</strong>, <em>Agencia Nacional de Investigación y Desarrollo, Chile</em></span>
      <span class="cv-right">2024 &ndash; 2026</span>
    </div>
  </div>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>Graduated with Highest Honors</strong>, <em>Universidad Mayor de San Andrés, Bolivia</em></span>
      <span class="cv-right">2022</span>
    </div>
  </div>
</div>

<div class="cv-section">
  <h2>Publications</h2>
  
  <h3 style="font-size: 1.1em; margin-bottom: 0.5em;">Submitted</h3>
  <ol reversed class="cv-enum">
  {% for post in site.publications reversed %}
    {% if post.status == 'submitted' %}
      <li>
        <div class="cv-details">
          <span class="cv-left">{{ post.citation }}</span>
          {% if post.paperurl %}
            <span class="cv-right"><a href="{{ post.paperurl }}" class="cv-link"><strong>[arXiv]</strong></a></span>
          {% endif %}
        </div>
      </li>
    {% endif %}
  {% endfor %}
  </ol>
  
  <h3 style="font-size: 1.1em; margin-bottom: 0.5em;">In Progress</h3>
  <ol reversed class="cv-enum">
  {% for post in site.publications reversed %}
    {% if post.status == 'in progress' %}
      <li>
        <div class="cv-details">
          <span class="cv-left">{{ post.citation }}</span>
        </div>
      </li>
    {% endif %}
  {% endfor %}
  </ol>
</div>

<div class="cv-section">
  <h2>Selected Talks</h2>
  
  <ol reversed class="cv-enum">
  {% for post in site.talks reversed %}
    {% if post.type == 'Invited Talk' or post.type == 'Contributed Talk' %}
      <li>
        <div class="cv-details">
          <span class="cv-left">
            <a href="{{ base_path }}{{ post.url }}" class="cv-link"><strong>{{ post.title }}</strong></a><br>
            <em>{{ post.venue }}</em> &mdash; {{ post.location }}
          </span>
          <span class="cv-right">{{ post.date | date: "%b %Y" }}</span>
        </div>
      </li>
    {% endif %}
  {% endfor %}
  </ol>
</div>

<div class="cv-section">
  <h2>Teaching Experience</h2>
  
  <ol reversed class="cv-enum">
  {% for post in site.teaching reversed %}
    {% if post.type contains 'Instructor' %}
      <li>
        <div class="cv-details">
          <span class="cv-left">
            <a href="{{ base_path }}{{ post.url }}" class="cv-link"><strong>{{ post.title }}</strong></a><br>
            <em>{{ post.type }}</em>, {{ post.venue }}
          </span>
          <span class="cv-right">{{ post.term }}</span>
        </div>
      </li>
    {% endif %}
  {% endfor %}
  </ol>
</div>

<div class="cv-section">
  <h2>Professional Service & Outreach</h2>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>Summer Course Coorganizer</strong>, <em>Geometría en las Alturas</em> (Intensive 3-day school)</span>
      <span class="cv-right">Feb 2026</span>
    </div>
    <ul class="cv-sublist"><li>Universidad Mayor de San Andrés, Bolivia (~60 participants).</li></ul>
  </div>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>Workshop Coorganizer</strong>, <em>Topology and Clay</em></span>
      <span class="cv-right">Sep 2024</span>
    </div>
    <ul class="cv-sublist"><li>Pontificia Universidad Católica de Chile.</li></ul>
  </div>
  
  <div class="cv-item">
    <div class="cv-details">
      <span class="cv-left"><strong>Seminar Coorganizer</strong>, <em>Seminario de Estudiantes de Postgrado en Matemáticas</em></span>
      <span class="cv-right">2023 &ndash; 2024</span>
    </div>
    <ul class="cv-sublist"><li>Pontificia Universidad Católica de Chile (~30 participants).</li></ul>
  </div>
</div>

<div class="cv-section">
  <h2>Computer Skills</h2>
  <ul class="cv-sublist" style="list-style-type: none; padding-left: 0;">
    <li><strong>Software:</strong> MATHEMATICA, Python, Julia.</li>
    <li><strong>Markup Languages:</strong> LaTeX, HTML, Markdown.</li>
    <li><strong>Development:</strong> GitHub (Custom calculation scripts for ℚHD discrepancies and M-resolutions).</li>
  </ul>
</div>