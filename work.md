---
layout: media
permalink: /work/
title: "Latest Posts"
page.share: false
---

<div class="tiles">
{% for post in site.posts %}
	{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
