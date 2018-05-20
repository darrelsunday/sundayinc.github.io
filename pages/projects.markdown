---
title: Projects
permalink: "/projects/"
layout: default
---

# Projects

<!--
DO NOT EDIT BELOW THIS LINE
-->

<div>
	{% for project in site.projects %}
	<span>{{ project.date | date_to_string }} - {{ project.title }}</span>
	{% endfor %}
</div>