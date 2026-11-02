---
layout: page
title: call for papers
permalink: /call-for-papers/
description: Non-archival submissions to both workshop tracks, managed through OpenReview.
nav: true
nav_order: 1
---

We invite **non-archival papers of up to eight pages, including references**. Position papers and preliminary or negative results are
welcome. Submissions may address [Track 1, Track 2, or both]({{ '/' | relative_url }}#two-complementary-tracks). Both tracks share one review
process.

Accepted papers will be presented as posters, and a selection will be invited for short spotlight talks. Accepted papers will be posted on
this website before the workshop.

## Topics

Across both tracks, we welcome work on:

- Data- and interaction-efficient learning under limited computation and memory.
- Retaining previous skills, mitigating catastrophic forgetting, and preserving plasticity across successive tasks and environmental changes.
- How policy design, learning objectives, and prior experience influence the ability to acquire new capabilities and adapt.
- Monitoring performance, diagnosing and recovering from failures, and maintaining safety during adaptation.
- Metrics and benchmarks for adaptability, retention, and learning efficiency, including whether offline evaluations predict performance
  during real-world deployment.

## Important dates

| Event | Date |
| :---- | :--- |
{% for d in site.data.workshop.important_dates -%}
| {{ d.event }} | {{ d.date }} |
{% endfor %}

## Submission

Submissions are managed through **OpenReview**.
{% if site.data.workshop.submission_url %}Submit your paper at [{{ site.data.workshop.submission_url }}]({{ site.data.workshop.submission_url }}).{% else %}The
submission link will be posted here when the call opens.{% endif %}

- **Length:** up to eight pages, including references.
- **Archival status:** non-archival.
- **Review:** reviews and acceptance decisions will be released at least six weeks before the conference.

## Inclusion

We especially welcome submissions from groups with limited access to robots or computational resources, and from students and early-career
researchers. Spotlight selection considers contribution quality and balance across the two tracks.

## Best Poster Award

We plan a Best Poster Award, which will be announced at the end of the workshop. This is a workshop award and is distinct from the official
ICRA conference awards.

Questions? Email [{{ site.email }}](mailto:{{ site.email }}).
