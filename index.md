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

### Installation Engineer, [Oblong Industries, Inc]( https://oblong.com/ ); Los Angeles, CA – 2012
Deployed [Mezzanine™]( https://vimeo.com/34861262 ) multi-user, multi-screen, multi-device room collaboration system.

### [Mac Genius™]( https://apple.com/retail/geniusbar/ ), [Apple Inc]( https://apple.com ); Rancho Cucamonga, CA – 2005–2009
Repair and user support for Apple devices: Mac, iPhone, &c.

## Education
<ul>
  {% for degree in site.degrees reversed %}
    <li>
      <h3 id="{{ degree.url | split: '/' | last | split: '.' | first }}"><a href="{{ degree.link }}">{{ degree.institution }}</a></h3>
      <a href="{{ degree.detailLink }}">{{ degree.title }}</a>, <time datetime="{{ degree.date }}">{{ degree.date | date: "%Y" }}</time>
      {{ degree.excerpt }}
    </li>
  {% endfor %}
</ul>

## Skills
Extensive experience with Active Directory Domain Services + Certificate Services, Azure Active Directory, Azure MFA, Azure Application Proxy, Azure Information Protection, Microsoft Defender for Endpoint, Windows client and server deployment, Group Policy Management, Remote Desktop Services, Google Workspace (“G Suite”), Microsoft Endpoint Manager (Intune), Hyper-V, Windows Failover Clustering, and VMware vSphere ESXi, as well as core technologies including TPM, Virtualization-based Security, Kerberos, Group Managed Service Accounts, and related.

