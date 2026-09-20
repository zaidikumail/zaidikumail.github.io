---
layout: page
permalink: /talks/
title: talks
description: Talks given
nav: true
nav_order: 3
---

<div class="talks">
{% assign sorted_talks = site.data.talks | sort: "date" | reverse %}
{% for talk in sorted_talks %}
  <div class="talk-entry" style="margin-bottom: 1em;">
    <strong>
      {% if talk.url %}
        <a href="{{ talk.url }}">{{ talk.title }}</a>
      {% else %}
        {{ talk.title }}
      {% endif %}
    </strong><br>
    {% if talk.type %}{{ talk.type }} — {% endif %}{{ talk.location }} ({{ talk.date | date: "%B %Y" }}){% if talk.note %} <em>({{ talk.note }})</em>{% endif %}
  </div>
{% endfor %}
</div>