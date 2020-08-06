---
layout: concertina
title: Architecture
---

# {{ page.title }}

## Arch docs

| Title | Description |
|-------|-------------|
{% for f in site.arch %}{% assign parts = f.url | split: '/' %}{% if parts.size != 3 %}{% continue %}{% endif %}[{{f.title}}]({{f.url}}) | {{ f.description }}
{% endfor %}

