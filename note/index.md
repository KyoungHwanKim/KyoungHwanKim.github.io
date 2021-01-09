---
layout: default
title: "Note"
description: 공부 합시다.
main: true
project-header: true
header-img: 
---
<ul class="catalogue">
{% assign sorted = site.pages | sort: 'order' | reverse %}
{% for page in sorted %}
{% if page.note == true %}
{% include post-list.html %}
{% endif %}
{% endfor %}
</ul>