---
layout: concertina
title: Diagram
description: Diagrams of the Architecture
author: flatcap
---

# {{ page.title }}

{:.subtitle}
{{ page.description }}

<table summary="diagrams of the architecture">
  <thead>
    <tr>
      <th>Page</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    {% for page in site.arch %}
      {% assign parts = page.url | split: '/' %}
      {% if parts.size == 4 and parts[2] == 'diagram' %}
      <tr>
        <td><a href="{{ page.url }}">{{ page.title }}</a></td>
        <td>{{page.description}}</td>
      </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>

