---
permalink: /
title: "Applied & Computational Mathematics Seminar"
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---

The SNU Applied and Computational Mathematics seminar brings together researchers to explore how mathematical tools can be used to solve real-world problems. The talks are delivered in a casual setting by both internal and external speakers, covering a variety of subjects like computational science, machine learning, and physical science. The goal is to provide a broad overview of topics that appeal to a diverse audience. 

## Announcement
Please note that the seminar scheduled for June 12th has been rescheduled to Monday, June 15th. <br>
The time remains unchanged, from 10:30AM to 12:00PM(GMT+9, KST).

## Upcoming Seminar

{% assign today = 'now' | date: '%s' %}
{% assign upcoming_talks = site.talks | sort: 'date' %}
{% assign has_upcoming = false %}

{% for talk in upcoming_talks %}
{% assign talk_date = talk.date | date: '%s' %}
{% if talk_date >= today %}
<div class="notice--info">
<p><a href="{{ talk.url }}">{{ talk.title }}</a></p>
<p>Date : {{ talk.date | date: "%B %-d, %Y" }} </p><br>
</div>
{% assign has_upcoming = true %}
{% break %}
{% endif %}
{% endfor %}

---

To receive email notifications about the schedules and abstracts of the ACM seminars, you can join our mailing list [here](/mailing-list/).
