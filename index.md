---
layout: default
permalink: /
title: "Latest Posts"
image:
  feature: home-feature.jpg
---
{% if page.image.feature %}
<div class="page-feature">
	<div class="page-image">
		<img src="{{ site.url }}/images/{{ page.image.feature }}" class="page-feature-image" alt="{{ page.title }}" itemprop="image">
		{% if page.image.credit %}{% include image-credit.html %}{% endif %}
	</div><!-- /.page-image -->
</div><!-- /.page-feature -->
{% endif %}

<div class="tiles">
{% for post in site.posts %}
	{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
