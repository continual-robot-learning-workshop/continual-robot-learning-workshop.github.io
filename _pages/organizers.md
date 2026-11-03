---
layout: page
title: organizers
permalink: /organizers/
description: Organizing committee and advisory board.
nav: true
nav_order: 4
_styles: >
  .person-photo { width: 130px; height: 130px; object-fit: cover; object-position: center 30%; }
  .person-initials { width: 130px; height: 130px; display: inline-flex; align-items: center; justify-content: center;
  font-size: 2.2rem; color: var(--global-text-color-light); background: var(--global-divider-color); }
  .person-link { font-size: 0.85rem; overflow-wrap: anywhere; }
  .person-link a::after { display: none; }
---

## Organizing committee

<div class="row">
{%- for p in site.data.organizers.committee %}
  <div class="col-6 col-sm-4 text-center mb-4">
    {%- if p.image %}
    <img src="{{ p.image | prepend: '/assets/img/organizers/' | relative_url }}" alt="{{ p.name }}" class="person-photo rounded-circle mb-2" loading="lazy">
    {%- else %}
    {%- assign parts = p.name | split: " " %}
    <div class="person-initials rounded-circle mb-2" aria-hidden="true">{{ parts.first | slice: 0 }}{{ parts.last | slice: 0 }}</div>
    {%- endif %}
    <div><strong>{% if p.url %}<a href="{{ p.url }}">{{ p.name }}</a>{% else %}{{ p.name }}{% endif %}</strong></div>
    <div>{{ p.affiliation }}</div>
    {%- if p.url %}
    {%- assign host = p.url | remove_first: 'https://' | remove_first: 'http://' | remove_first: 'www.' | split: '/' | first %}
    <div class="person-link"><a href="{{ p.url }}"><i class="fa-solid fa-link"></i> {{ host }}</a></div>
    {%- endif %}
  </div>
{%- endfor %}
</div>

## Organizing experience

Members of the organizing committee bring experience from related workshops and community events:

{% for e in site.data.organizers.experience -%}
- **{{ e.name }}** {{ e.events }}
{% endfor %}

## Advisory board

The advisory board advises on speakers, review criteria, and the research agenda. Operational responsibility for the workshop remains with
the organizing committee.

<div class="row">
{%- for p in site.data.organizers.advisory %}
  <div class="col-6 col-sm-4 text-center mb-4">
    {%- if p.image %}
    <img src="{{ p.image | prepend: '/assets/img/organizers/' | relative_url }}" alt="{{ p.name }}" class="person-photo rounded-circle mb-2" loading="lazy">
    {%- endif %}
    <div><strong>{% if p.url %}<a href="{{ p.url }}">{{ p.name }}</a>{% else %}{{ p.name }}{% endif %}</strong></div>
    <div>{{ p.affiliation }}</div>
    {%- if p.url %}
    {%- assign host = p.url | remove_first: 'https://' | remove_first: 'http://' | remove_first: 'www.' | split: '/' | first %}
    <div class="person-link"><a href="{{ p.url }}"><i class="fa-solid fa-link"></i> {{ host }}</a></div>
    {%- endif %}
  </div>
{%- endfor %}
</div>

## Contact

Reach the organizers at [{{ site.email }}](mailto:{{ site.email }}).
