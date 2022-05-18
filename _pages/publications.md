---
layout: page
permalink: /publications/
title: Publications
description: List of accepted and submitted research works.
published_years: [2022, 2021]
submitted_years: [2021, 2022]
display_categories: [published, review]
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">
{%- if page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
    {%- if category == "published" %}
      <h2 class="category">Accepted publications</h2>
      {%- for y in page.published_years %}
        <h2 class="year">{{y}}</h2>
        {% bibliography -f papers -q @*[year={{y}} && category={{category}}]* %}
      {% endfor %}
    {% else %}
      <br><br>
      <h2 class="category">Under Review</h2>
      {%- for y in page.submitted_years %}
        <h2 class="year">{{y}}</h2>
        {% bibliography -f papers -q @*[year={{y}} && category={{category}}]* %}
      {% endfor %}
    {% endif %}
  {%- endfor %}
{%- endif -%}
</div>