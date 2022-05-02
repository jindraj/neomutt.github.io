---
title: News
---

# {{ page.title }}

Please check the release page for any updates.

{%for post in site.posts %}
    {% unless post.next %}
## {{ post.date | date: '%B %Y' }}
    {% else %}
        {% capture year %}{{ post.date | date: '%Y %m' }}{% endcapture %}
        {% capture nyear %}{{ post.next.date | date: '%Y %m' }}{% endcapture %}
        {% if year != nyear %}
## {{ post.date | date: '%B %Y' }}
        {% endif %}
    {% endunless %}
- [{{ post.date | date: "%b %d" }} - {{ post.title }}]({{ post.url }})
{% endfor %}
