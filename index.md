---
title: Résumé
layout: about
---

{% assign about_me = site.pages | where:"name","about.md" | first %}
{{ about_me.excerpt | default: about_me.content | split: site.excerpt_separator | first }}

## Experience
<ul>
{% for job in site.jobs reversed %}
  <li>
    <h3 id="{{ job.url | split: '/' | last | split: '.' | first }}"><a href="{{ job.link }}">{{ job.employer }}</a></h3>
    <a href="{{ job.detailLink }}">{{ job.title }}</a>, <time datetime="{{ job.date }}">{{ job.date | date: "%Y" }}</time> -- <time datetime="{{ job.endDate }}">{{ job.endDate | date: "%Y" }}</time>
    {{ job.excerpt }}
  </li>
{% endfor %}
</ul>

## Education
<ul>
{% for degree in site.degrees reversed %}
  <li id="{{ degree.slug }}">
    <h3 id="{{ degree.institution | slugify }}"><a href="{{ degree.link }}">{{ degree.institution }}</a></h3>
    <a href="{{ degree.detailLink }}">{{ degree.title }}</a>, <time datetime="{{ degree.date }}">{{ degree.date | date: "%Y" }}</time>
    {{ degree.excerpt }}
  </li>
{% endfor %}
</ul>

## Certifications
{% assign certifiers = site.certifications | map: 'certifier' | uniq %}
{% if certifiers | size > 1 %}
<ul class="plist">
{% for certifier in certifiers %}
    <li id="{{ certifier | slugify }}">{{ certifier }}</li>
{% endfor %}
</ul>
{% endif %}
<ul>
{% for certificate in site.certifications reversed %}
      <li id="{{ certificate.slug }}">
      <a href="{{ certificate.link }}">{{ certificate.track }}: {{ certificate.title }}</a> <a href="{{ certificate.detailLink }}">{{ certificate.level | capitalize }}, <time datetime="{{ certificate.date }}">{{ certificate.date | date: "%Y" }}</time></a>
      {{ certificate.excerpt }}
      </li>
{% endfor %}
</ul>

## Skills
{% assign skills = site.tags | concat: site.certifications | concat: site.jobs | concat: site.projects | map: 'tags' | uniq | sort %}
<ul class="plist">
{% for skill in skills %}
    <li>{{ skill }}</li>
{% endfor %}
</ul>
