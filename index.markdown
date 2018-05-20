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

<div class="recent-projects">
	<span class="recent-projects__header">Recent Projects</span>
	<div class="recent-projects__container">
		{% for project in site.posts limit:3 %}
		<a class="recent-projects__item" href="{{ project.url }}">
			<span class="recent-projects__item__title">{{ project.title }}</span>
			<span class="recent-projects__item__date">{{ project.date | date_to_string }}</span>
		</a>
		{% endfor %}
	</div>
	<span class="recent-projects__footer"><a href="/projects">All projects &rarr;</a></span>
</div>