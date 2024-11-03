---
layout: home2
title: about
permalink: /
description: 
display_categories: [research]
---

<!--Banner image-->
<div class="row mb-5">
    <div class="col-sm mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Boiga-angulata-banner.jpg" title="Boiga angulata" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<!--About me (left) and photo right-->
<div class="row justify-content-sm-center mb-2">
    <!--left page margin-->
    <div class="col-sm-2 mt-3 mt-md-0">
    </div>
    <!--text column-->
    <div class="col-sm-5 mt-3 mt-md-0">
        <div class="row"><h1 class="post-title">About Me</h1></div>
        <div class="row">I am a NSF Postdoctoral Fellow and Mentor at the American Museum of Natural History in New York, where I investigate genomics and evolution of reptiles. I have 10 years of experience learning and working in natural history museums with major biodiversity collections to study a broad range of questions.</div>
    </div>
    <!--photo column-->
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/jeff3.jpg" title="Jeffrey Weinell" class="img-fluid rounded z-depth-1" %}
    </div>
    <!--right page margin-->
    <div class="col-sm-2 mt-3 mt-md-0">
    </div>
</div>


<!--Research-->
<div class="row justify-content-sm-center mb-5">
    <!--left page margin-->
    <div class="col-sm-2 mt-md-0">
    </div>
    <!--text column-->
    <div class="col-sm-4 mt-md-0">
        <div class="row"><h1 class="post-title">Research Interests</h1></div>
        <div class="row">I integrate genomic, organismal, and ecological data with advanced computational methods to investigate how biodiversity is generated and maintained in nature.</div>
    </div>
    <!--first photo column-->
    <div class="col-sm-1 mt-md-0">
        <div class="row justify-content-sm-center">
        </div>
    </div>
    <!--second photo column-->
    <div class="col-sm-3 mt-md-0">
        <div class="row justify-content-sm-center">
            <!--first row of first column column-->
            <div class="row">{% include figure.liquid path="assets/img/Aplopeltura-boa_SanRafael-Samar_2018_JLW.jpg" title="Aplopeltura boa" class="img-fluid rounded z-depth-1" %}</div>
        </div>
    </div>
    <!--right page margin-->
    <div class="col-sm-2 mt-md-0">
    </div>
</div>

<div class="row justify-content-sm-center">
    <!--left page margin-->
    <div class="col-sm-2 mt-md-0">
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Trimeresurus-flavomaculatus_MWH282_Cabadbaran-Mindanao_Dec2019.jpg" title="Trimeresurus flavomaculatus" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/KarstForest_SanRafael-Samar_2018_RKA.jpg" title="Samar Island Karst forest" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Oxyrhabdium-modestum_Mindanao-Endemic-Clade_MWH377_AgusanMarsh_December2019_DSC_7089.jpg" title="Oxyrhabdium modestum" class="img-fluid rounded z-depth-1" %}
    </div>
    <!--right page margin-->
    <div class="col-sm-2 mt-md-0">
    </div>
</div>

<!-- projects -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>


