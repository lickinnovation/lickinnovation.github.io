---
layout: default
permalink: /
title: "Home"
image:
  feature: home-feature-bulb.jpg
---
{% if page.image.feature %}

  <div class="page-lead" style="background-image:url({{ site.url }}/images/{{ page.image.feature }})">
		<div class="wrap page-lead-content">
		  <h1>Lick Innovation</h1>
			<h2>A catchy slogan</h2>
			<a href="{{ site.url }}/work" class="btn-inverse">See our work</a>
			{% if page.image.credit %}{% include image-credit.html %}{% endif %}
		</div><!-- /.page-lead-content -->
</div><!-- /.page-lead -->
{% endif %}

<div class="archive-wrap">
  <div class="page-title">
    <h1></h1>
  </div>
{% for product in site.products %}
	<article class="tile" itemscope itemtype="http://schema.org/Article">
		<a href="{{ site.url }}{{ product.url }}" title="{{ product.title }}" class="post-teaser">{% if product.image.teaser %}<img src="{{ site.url }}/images/{{ product.image.teaser }}" alt="teaser" itemprop="image">
			{% else %}<img src="{{ site.url }}/images/{{ site.teaser }}" alt="teaser" itemprop="image">{% endif %}</a>
		<h2 class="post-title" itemprop="name"><a href="{{ site.url }}{{ product.url }}">{{ product.title }}</a></h2>
  </article><!-- /.tile -->
  {% endfor %}
</div><!-- /.archive-wrap -->
