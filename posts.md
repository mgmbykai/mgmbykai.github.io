---
layout: archive
title: "Posts"
permalink: /posts/
author_profile: true
entries_layout: list
---

{% for post in site.posts %}
  {% include archive-single.html %}
{% endfor %}