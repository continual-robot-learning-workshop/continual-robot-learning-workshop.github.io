---
layout: about
title: home
permalink: /
subtitle: >
  <b>Continual Robot Learning After Deployment</b><br>
  ICRA 2027 Workshop &middot; Seoul, South Korea &middot; Full day, in person

selected_papers: false
social: true # contact icons from _data/socials.yml

announcements:
  enabled: false # news is rendered from _data/workshop.yml below

latest_posts:
  enabled: false
---

Recent advances in learning-based robot control have expanded the range of tasks robots can perform. Reliable long-term deployment, however,
requires robots to **continually adapt to changing conditions while retaining existing capabilities**. Recent work on continual manipulation,
locomotion, and autonomous navigation shows progress toward this goal, yet continual robot learning in the real world may still require
rethinking some long-standing assumptions in our field.

This workshop brings together researchers who **adapt pretrained policies** and researchers who study **continual learning from robot
interaction**, to identify shared challenges and evaluation priorities. The workshop is endorsed by the **IEEE RAS Technical Committee on
Robot Learning**.

## Two complementary tracks

**Track 1: Adapting pretrained general-purpose policies.** Post-training from demonstrations, corrections, preferences, rewards, and
rollouts, including adaptation through parameters, context, memory, retrieval, and reusable skill acquisition.

**Track 2: Continual learning from experience.** Continuously learning from robot interaction without requiring a pretrained policy, with a
focus on knowledge acquisition and adaptation under limited interaction, computational resources, and safety constraints.

Submissions may address either track or both. The two tracks share one review process, the poster sessions, and the discussion.

## Shared research questions

1. When should a robot learn, which components should change, and what feedback should guide the update?
2. How do prior training and experience shape a robot's ability to acquire and reuse knowledge efficiently while retaining competence and
   plasticity under limited interaction, computation, and memory?
3. How should learning be monitored and evaluated across successive updates, and what evidence justifies safe continued deployment or
   recovery?

The discussions will feed into a **shared research agenda** of priorities and practical guidelines for designing and evaluating continually
learning robots, published by the organizers after the workshop.

## Important dates

| Event | Date |
| :---- | :--- |
{% for d in site.data.workshop.important_dates -%}
| {{ d.event }} | {{ d.date }} |
{% endfor %}

See the [call for papers]({{ '/call-for-papers/' | relative_url }}) for submission details and the [program]({{ '/program/' | relative_url }})
for the full-day schedule.

## News

{% for item in site.data.workshop.news %}
- **{{ item.date }}**: {{ item.text }}
{% endfor %}
