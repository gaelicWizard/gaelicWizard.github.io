---
title: Résumé
---

Experienced systems architect seeking forward-looking position to drive adoption of modern information systems in identity management, server deployment, and device configuration. I believe strongly that the best operations teams are always in motion building small improvements at all levels; stasis breeds complacency and leads to decay. 

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
  {% for institution in site.degrees reversed %}
    <li>
      <h3 id="{{ institution.institution | slugify }}"><a href="{{ institution.link }}">{{ institution.institution }}</a></h3>
      <ul>
    {% for degree in site.degrees reversed %}
      {% if degree.institution contains institution.institution %} 

      <li id="{{ degree.slug }}">
      <a href="{{ degree.detailLink }}">{{ degree.title }}</a>, <time datetime="{{ degree.date }}">{{ degree.date | date: "%Y" }}</time>
      {{ degree.excerpt }}
      </li>

      {% endif %}
    {% endfor %}
    </ul>
    </li>
  {% endfor %}
</ul>

## Certifications
<ul>
  {% assign certifiers = site.certifications | map: 'certifier' | uniq %}
  {% for certifier in certifiers %}
    <li>
      <h3 id="{{ certifier | slugify }}">{{ certifier }}</h3>
      <ul>
    {% for certificate in site.certifications reversed | where: 'certifier', certifier %}

      <li id="{{ certificate.slug }}">
      <a href="{{ certificate.link }}">{{ certificate.track }}: {{ certificate.title }}</a> <a href="{{ certificate.detailLink }}">{{ certificate.level | capitalize }}, <time datetime="{{ certificate.date }}">{{ certificate.date | date: "%Y" }}</time></a>
      {{ certificate.excerpt }}
      </li>

    {% endfor %}
    </ul>
    </li>
  {% endfor %}
</ul>

## Skills
Extensive experience with Active Directory Domain Services + Certificate Services, Azure Active Directory, Azure MFA, Azure Application Proxy, Azure Information Protection, Microsoft Defender for Endpoint, Windows client and server deployment, Group Policy Management, Remote Desktop Services, Google Workspace (“G Suite”), Microsoft Endpoint Manager (Intune), Hyper-V, Windows Failover Clustering, and VMware vSphere ESXi, as well as core technologies including TPM, Virtualization-based Security, Kerberos, Group Managed Service Accounts, and related.

