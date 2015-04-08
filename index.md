---
layout: default
permalink: /
title: "Latest Posts"
image:
  feature: home-feature-tall.jpg
---
{% if page.image.feature %}
<div class="page-lead" style="background-image:url({{ site.url }}/images/{{ page.image.feature }})">
	<div class="wrap page-lead-content">
		{% if page.image.credit %}{% include image-credit.html %}{% endif %}
	</div><!-- /.page-lead-content -->
</div><!-- /.page-lead -->
{% endif %}

<div class="wrap">
<div class="tiles">
{% for post in site.posts %}
	{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
</div><!-- /.wrap -->
