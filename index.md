---
layout: default
permalink: /
title: "Home"
image:
  feature: home-feature-tall.jpg
---
{% if page.image.feature %}
<div class="page-lead" style="background-image:url({{ site.url }}/images/{{ page.image.feature }})">
	<div class="wrap page-lead-content">
	  <h1>Lick Innovations</h1>
		<h2>A catchy slogan</h2>
		<a href="{{ site.url }}/work" class="btn">See our work</a>
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
