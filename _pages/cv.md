---
layout: page2
title: cv
permalink: /cv/
nav: true
nav_order: 4
toc:
  sidebar: left
---

<!--Banner image-->
<div class="row mb-5">
    <div class="col-sm mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cerrado-banner.jpg" title="Cerrado banner" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<!--page title-->
<div class="row justify-content-sm-center">
    <div class="col-sm-2 mt-md-0">
    </div>
    <div class="col-sm-8 mt-md-0">
        <!--cv title-->
        <div class="row">
            <h1 class="post-title">
            CV&nbsp;&nbsp;
            <a href="https://jeffweinell.github.io/assets/pdf/Weinell-Jeffrey_CV.pdf"
               target="_blank"
               rel="noopener noreferrer"
               class="float-right" >
               <i class="fa-solid fa-file-pdf"></i>
            </a>
            </h1>
        </div>
        <article>
          <div class="cv">
            {% for entry in site.data.cv %}
              <a class="anchor" id="{{ entry.title }}"></a>
              <div class="card mt-3 p-3">
                <h3 class="card-title font-weight-medium">{{ entry.title }}</h3>
                <div>
                  {% if entry.type == 'list' %}
                    {% include cv/list.liquid %}
                  {% elsif entry.type == 'map' %}
                    {% include cv/map.liquid %}
                  {% elsif entry.type == 'nested_list' %}
                    {% include cv/nested_list.liquid %}
                  {% elsif entry.type == 'time_table' %}
                    {% include cv/time_table.liquid %}
                  {% elsif entry.type == 'list_groups' %}
                    {% include cv/list_groups.liquid %}
                  {% else %}
                    {{ entry.contents }}
                  {% endif %}
                </div>
              </div>
            {% endfor %}
          </div>
        </article>
    </div>
    <div class="col-sm-2 mt-md-0">
    </div>
</div>







