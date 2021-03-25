---
title: "Post about Algorism"
layout: archive
permalink: /categories/Algorism
author_profile: true
sidebar_main: true
---

{% assign posts = site.categories.Algorism | sort:"date" %}

{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}
