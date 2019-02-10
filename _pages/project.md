---
permalink: /project/
title: "Independent Project"
author_profile: true
---

{% include base_path %}

{% for project in site.projects reversed %}
  {% include archive-single.html %}
{% endfor %}