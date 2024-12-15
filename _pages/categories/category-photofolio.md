---
title: "photofolio"
layout: archive
permalink: categories/photofolio
author_profile: true
sidebar_main: true
---

{% assign posts = site.categories.photofolio %}

{% for post in posts %} {% include archive-single2.html type=page.entries_layout %}{% endfor %}
