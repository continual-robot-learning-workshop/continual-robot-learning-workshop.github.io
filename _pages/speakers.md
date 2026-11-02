---
layout: page
title: speakers
permalink: /speakers/
description: Invited speakers and panelists. All talks are in person.
nav: true
nav_order: 3
_styles: >
  .person-photo { width: 150px; height: 150px; object-fit: cover; object-position: center 30%; }
---

{% assign groups = "track1,bridging,track2,panel" | split: "," %}
{% for key in groups %}
{% assign group = site.data.speakers[key] %}

<h2>{{ group.title }}</h2>
<div class="row">
{%- for p in group.people %}
  <div class="col-6 col-sm-4 text-center mb-4">
    {%- if p.image %}
    <img src="{{ p.image | prepend: '/assets/img/speakers/' | relative_url }}" alt="{{ p.name }}" class="person-photo rounded-circle mb-2" loading="lazy">
    {%- endif %}
    <div><strong>{% if p.url %}<a href="{{ p.url }}">{{ p.name }}</a>{% else %}{{ p.name }}{% endif %}</strong></div>
    <div>{{ p.affiliation }}</div>
    {%- if p.topic %}<div><em>{{ p.topic }}</em></div>{% endif %}
    {%- if p.tbc %}<div><em>(to be confirmed)</em></div>{% endif %}
  </div>
{%- endfor %}
</div>
{% endfor %}

See the [program]({{ '/program/' | relative_url }}) for session times.
