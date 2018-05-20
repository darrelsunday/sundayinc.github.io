---
permalink: "/projects/"
layout: default
---

# Projects

<!--
DO NOT EDIT BELOW THIS LINE
-->

<div>
	{% assign sorted = (site.projects | sort: 'date') | reverse %}
	{% for project in sorted %}
	<span>{{ project.date | date_to_string }} - {{ project.title }}</span>
	{% endfor %}
</div>