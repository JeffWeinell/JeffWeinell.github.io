---
layout: page2
title: publications
permalink: /publications/
description: 
nav: true
nav_order: 3
---

<!--Banner image-->
<div class="row mb-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Lipinia-pulcherra-banner.jpg" title="Lipinia pulcherra banner" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<!--page title-->
<div class="row justify-content-sm-center">
    <div class="col-sm-2 mt-3 mt-md-0">
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        <h1 class="post-title">{{ page.title }}</h1>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
    </div>
</div>

<!--Bibsearch Feature-->
<div class="row justify-content-sm-center">
    <div class="col-sm-2 mt-3 mt-md-0">
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include bib_search.liquid %}
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
    </div>
</div>

<!--bibliography-->
<div class="row justify-content-sm-center">
    <div class="col-sm-2 mt-3 mt-md-0">
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        <div class="publications">
            {% bibliography %}
        </div>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
    </div>
</div>

