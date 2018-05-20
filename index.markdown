---
layout: default
---

{% assign ABOUT_TEXT = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec 
efficitur nunc arcu, non vestibulum mi consequat at. Donec pulvinar 
faucibus auctor. Ut vel neque vel nibh tincidunt tristique. Maecenas 
tristique quam purus, ac condimentum lorem imperdiet a. In ut vehicula 
massa. Mauris bibendum diam orci, nec lacinia leo ultrices a. Praesent 
et magna vulputate, ultrices ligula vel, rhoncus ex. Proin molestie ipsum 
vel tortor sollicitudin, nec porttitor quam porta. In et nisl ac eros dapibus 
lacinia.' %}

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