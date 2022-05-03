---
title: Résumé
layout: about
---

{% assign about_me = site.pages | where:"name","about.md" | first %}
<p class="p-summary">{{ about_me.excerpt | default: about_me.content | split: site.excerpt_separator | first | strip_html }}</p>

## Experience
<ul>{% for job in site.jobs reversed %}
  <li class="p-experience h-event">
    <h3 class="p-location h-card" id="{{ job.url | split: '/' | last | split: '.' | first }}"><a class="p-fn p-org u-url" href="{{ job.link }}">{{ job.employer }}</a></h3>
    <a class="p-name u-url" href="{{ job.detailLink }}">{{ job.title }}</a>, <time class="dt-start" datetime="{{ job.date | date: "%Y-%m-%d" }}">{{ job.date | date: "%Y" }}</time> -- <time class="dt-end" datetime="{{ job.endDate | date: "%Y-%m-%d" }}">{{ job.endDate | date: "%Y" }}</time>
    <p class="p-summary">{{ job.excerpt | strip_html }}</p>
  </li>
{% endfor %}</ul>

## Education
<ul>{% for degree in site.degrees reversed %}
  <li class="p-education h-event" id="{{ degree.slug }}">
    <h3 class="p-location h-card" id="{{ degree.institution | slugify }}"><a class="u-url p-fn p-org" href="{{ degree.link }}">{{ degree.institution }}</a></h3>
    <a class="p-name" href="{{ degree.detailLink }}">{{ degree.title }}</a>, <!--<time class="dt-start" datetime="">--><time class="dt-end" datetime="{{ degree.date | date: "%Y-%m-%d" }}">{{ degree.date | date: "%Y" }}</time>
    <p class="p-summary">{{ degree.excerpt | strip_html }}</p>
  </li>
{% endfor %}</ul>

## Certifications
{% assign certifiers = site.certifications | map: 'certifier' | uniq %}
{% if certifiers | size > 2 %}
<ul class="plist">{% for certifier in certifiers %}
  <li id="{{ certifier | slugify }}">{{ certifier }}</li>
{% endfor %}</ul>
{% endif %}
<ul>{% for certificate in site.certifications reversed %}
  <li class="p-skill" id="{{ certificate.slug }}">
    <a href="{{ certificate.link }}">{{ certificate.track }}: {{ certificate.title }}</a> <a href="{{ certificate.detailLink }}">{{ certificate.level | capitalize }}, <time class="dt-start" datetime="{{ certificate.date | date: "%Y-%m-%d" }}">{{ certificate.date | date: "%Y" }}</time></a>
    <p class="p-summary">{{ certificate.excerpt | strip_html }}</p>
  </li>
{% endfor %}</ul>

## Skills
{% assign skills = site.tags | concat: site.certifications | concat: site.jobs | concat: site.projects | map: 'tags' | uniq | sort %}
<ul class="plist">{% for skill in skills %}
  <li class="p-skill">{{ skill }}</li>
{% endfor %}</ul>
