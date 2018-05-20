---
title: Homepage
layout: default
---

<div class="about">
	<div class="about__image">
		<img src="/assets/sunday.jpg" alt="sunday">
	</div>
	<div class="about__content">
		<span class="about__content__name">Darrel Sunday</span>
		<span class="about__content__title">Environmental Advisor</span>
		<span class="about__content__text">
			{{ site.data.edit.about }}
		</span>
	</div>
</div>

<div class="recent-projects">
	<span class="recent-projects__header">Recent Projects</span>
	<div class="recent-projects__container">
		{% assign sorted = (site.projects | sort: 'date') | reverse %}
		{% for project in sorted limit:3 %}
		<a class="recent-projects__item" href="{{ project.url }}">
			<span class="recent-projects__item__title">{{ project.title }}</span>
			<span class="recent-projects__item__date">{{ project.date | date_to_string }}</span>
		</a>
		{% endfor %}
	</div>
	<span class="recent-projects__footer"><a href="/projects">All projects &rarr;</a></span>
</div>