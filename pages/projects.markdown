---
title: Projects
permalink: "/projects/"
layout: default
---

<div class="projects">
	<span class="projects__header">Projects</span>
	{% assign sorted = (site.projects | sort: 'date') | reverse %}
	{% for project in sorted limit:3 %}
	<div class="projects__item">
		<span class="projects__item__title">{{ project.title }}</span>
		<span class="projects__item__date">{{ project.date | date_to_string }}</span>
		<!--EXERPT-->
	</div>
	{% endfor %}
</div>