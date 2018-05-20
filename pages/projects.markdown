---
title: Projects
permalink: "/projects/"
layout: default
---

# Projects

<div>
	{% assign sorted = (site.projects | sort: 'date') | reverse %}
	{% for project in sorted %}
	<span>{{ project.date | date_to_string }} - {{ project.title }}</span>
	{% endfor %}
</div>