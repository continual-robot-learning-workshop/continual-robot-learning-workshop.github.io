---
layout: page
title: program
permalink: /program/
description: Full-day, in-person program. Workshop date and room to be announced.
nav: true
nav_order: 2
---

Each invited talk is 25 minutes followed by 5 minutes of questions. Coffee breaks double as poster time.

<table class="schedule">
  <thead>
    <tr><th>Time</th><th>Session</th></tr>
  </thead>
  <tbody>
  {%- for s in site.data.schedule %}
    <tr>
      <td style="white-space: nowrap">{{ s.time }}</td>
      <td>
        {%- if s.break %}<em>{{ s.title }}</em>{% else %}<strong>{{ s.title }}</strong>{% endif -%}
        {%- if s.details %}<br>{{ s.details }}{% endif -%}
        {%- if s.speakers %}
          {%- for p in site.data.speakers[s.speakers].people %}
            <br>{{ p.name }}{% if p.affiliation %} ({{ p.affiliation }}){% endif %}{% if p.topic %}: {{ p.topic }}{% endif %}{% if p.tbc %} <em>(to be confirmed)</em>{% endif %}
          {%- endfor %}
        {%- endif %}
      </td>
    </tr>
  {%- endfor %}
  </tbody>
</table>

More about the invited speakers is on the [speakers page]({{ '/speakers/' | relative_url }}).

## Deployment cases and panel discussion

The afternoon session combines the panel and the community discussion into a single case-based session. Each panelist briefly presents a
real-world case of continual robot learning, including its practical constraints, failures, and lessons learned. Two organizer-moderated
rounds then open the discussion to the audience, organized around the workshop's
[shared research questions]({{ '/' | relative_url }}#shared-research-questions).

The session ends with a group synthesis of the main challenges, open questions, and evaluation priorities. This synthesis will inform a
research agenda that the organizers will publish after the workshop.

## After the workshop

Slides and any available recordings will be shared here afterwards, with the consent of the speakers.
