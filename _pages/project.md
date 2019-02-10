---
layout: archive
title: "Independent Projects"
permalink: /project/
author_profile: true
---

{% include base_path %}

{% for post in site.projects reversed %}
  {% include archive-single.html %}
{% endfor %}