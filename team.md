---
layout: page
title: Meet The Team
permalink: /meet-the-team/
sidebar: none

---

{%- if include.title -%}
  <div class="uk-container uk-margin-medium-bottom">
    <hr class="uk-margin-remove">
    <h2 class="section-title uk-text-center uk-margin">{{- include.title -}}</h2>
    <hr class="uk-margin-remove">
  </div>
{%- endif -%}

<div class="uk-container uk-margin-medium-bottom uk-text-center">
  <div class="uk-child-width-1-2@s uk-child-width-expand@l uk-grid-medium uk-flex-center uk-grid-divider" data-uk-grid>
    {% for author in site.authors %}
      {% include content-team-author.html %}
    {% endfor %}
  </div>
</div>