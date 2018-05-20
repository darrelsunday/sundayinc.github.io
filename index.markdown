---
title: Homepage
layout: default
---

{% assign ABOUT_TEXT = "

About text...

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
	<span class="featured-services__header">Featured Services</span>
	<div class="featured-services__container">
		{% for service in site.services %}
		<span>{{ service.title }}</span>
		{% endfor %}
	</div>
</div>

<div class="recent-projects">
	<div class="recent-projects__content">
		<span class="recent-projects__content__header">Recent Projects</span>
		<div class="recent-projects__content__container">
			{% assign sorted = (site.projects | sort: 'date') | reverse %}
			{% for project in sorted limit:3 %}
			<a class="recent-projects__content__item" href="{{ project.url }}">{{ project.date | date_to_string }} - {{ project.title }}</a>
			{% endfor %}
		</div>
		<span class="recent-projects__content__footer"><a href="/projects">All projects &rarr;</a></span>
	</div>
	<div class="recent-projects__image">
		<img src="/assets/projects.jpg" alt="projects">
	</div>
</div>