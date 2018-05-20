---
title: Homepage
layout: default
---

{% assign ABOUT_TEXT = "

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut dapibus nibh 
turpis, vitae eleifend massa mattis facilisis. Integer feugiat vitae metus 
vulputate dapibus. Phasellus interdum odio eget mollis placerat. Quisque 
turpis justo, malesuada quis ipsum quis, varius iaculis nisl. Praesent 
ultricies eget lorem eget interdum. Pellentesque a dictum massa, ut dictum 
tellus. Orci varius natoque penatibus et magnis dis parturient montes, 
nascetur ridiculus mus. Curabitur maximus eget velit quis aliquam. Aenean sit 
amet euismod libero, vulputate consectetur ante.

" %}


{% assign SERVICES_TEXT = "

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut dapibus nibh 
turpis, vitae eleifend massa mattis facilisis. Integer feugiat vitae metus 
vulputate dapibus. Phasellus interdum odio eget mollis placerat. Quisque turpis 
justo, malesuada quis ipsum quis, varius iaculis nisl. Praesent ultricies eget 
lorem eget interdum. Pellentesque a dictum massa, ut dictum tellus. Orci varius 
natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Curabitur 
maximus eget velit quis aliquam.

" %}

<!--
DO NOT EDIT BELOW THIS LINE
-->

<div class="about">
	<div class="about__image">
		<img src="/assets/sunday.jpg" alt="sunday">
	</div>
	<div class="about__content">
		<span class="about__content__name">Darrel Sunday</span>
		<span class="about__content__title">Environmental Advisor</span>
		<span class="about__content__text">
			{{ ABOUT_TEXT }}
		</span>
	</div>
</div>

<div class="featured-services">
	<div class="featured-services__about">
		<span class="featured-services__about__header">Featured Services</span>
		<span class="featured-services__about__text">
				{{ SERVICES_TEXT }}
		</span>
		<span class="featured-services__about__all"><a href="/services">All services &rarr;</a></span>
	</div>
	<div class="featured-services__content">
		<div class="featured-services__content__container">
			{% for service in site.services %}
			<a class="featured-services__content__item" href="/services#{{ service.title }}">
				<span class="featured-services__content__item__text">{{ service.title }}</span>
			</a>
			{% endfor %}
		</div>
	</div>
</div>

<div class="recent-projects">
	<div class="recent-projects__image">
		<img src="/assets/projects.jpg" alt="projects">
	</div>
	<div class="recent-projects__content">
		<span class="recent-projects__content__header">Recent Projects</span>
		<div class="recent-projects__content__container">
			{% assign sorted = (site.projects | sort: 'date') | reverse %}
			{% for project in sorted limit:3 %}
			<a class="recent-projects__content__item" href="{{ project.url }}">{{ project.date | date_to_string }} - {{ project.title }}</a>
			{% endfor %}
		</div>
		<span class="recent-projects__content__all"><a href="/projects">All projects &rarr;</a></span>
	</div>
</div>