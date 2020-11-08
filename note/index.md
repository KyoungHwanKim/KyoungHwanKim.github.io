---
layout: default
title: "Note"
description: 공부는 죽을 때까지 하는 것.
main: true
project-header: true
header-img: None
---
<ul class="catalogue">
{% assign sorted = site.pages | sort: 'order' | reverse %}
{% for page in sorted %}
{% if page.note == true %}
{% include post-list.html %}
{% endif %}
{% endfor %}
</ul>