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
    <strong>{{ talk.title }}</strong><br>
    {{ talk.type }} — {{ talk.venue }}, {{ talk.location }} ({{ talk.date | date: "%B %Y" }})
  </div>
{% endfor %}
</div>