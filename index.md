---
title: Résumé
---

Experienced systems architect seeking forward-looking position to drive adoption of modern information systems in identity management, server deployment, and device configuration. I believe strongly that the best operations teams are always in motion building small improvements at all levels; stasis breeds complacency and leads to decay. 

## Experience
### Operator, Mayflower IS&T; Pasadena, CA – 2018—2021
As founder and principal of Mayflower, I collected requirements, designed solutions, and implemented deliverables at every layer of the IT stack for small medical practices in radiology and cardiology. Along with my team of two engineers, we supported and deployed Active Directory with Windows Hello, Azure AD with MFA and cloud password protection, Office 365, Mobile Device Management (Intune) for iOS and Mac, Remote Desktop Services for external access when necessary and Azure Application Proxy when possible, Google Workspace with SSO through Azure AD SAML, Hyper-V clusters with shared and converged storage, 3rd party application servers, Exchange Hybrid and Exchange Online, SharePoint Online, OneDrive for Business to replace Windows Roaming Profiles, Microsoft Teams, and more. We alsö leveraged Azure Log Analytics solutions for Desktop Analytics and Update Readiness, and were beginning Azure Sentinel.

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
### [Roger William University]( https://law.rwu.edu/ ); Bristol, RI – [Juris Doctor]( https://law.rwu.edu/academics/juris-doctor ), 2012
### [University of California]( https://ucr.edu/ ); Riverside, CA – [Bachelor of Arts / Law & Philosophy]( https://philosophy.ucr.edu/undergraduate-program ), 2009

## Skills
Extensive experience with Active Directory Domain Services + Certificate Services, Azure Active Directory, Azure MFA, Azure Application Proxy, Azure Information Protection, Microsoft Defender for Endpoint, Windows client and server deployment, Group Policy Management, Remote Desktop Services, Google Workspace (“G Suite”), Microsoft Endpoint Manager (Intune), Hyper-V, Windows Failover Clustering, and VMware vSphere ESXi, as well as core technologies including TPM, Virtualization-based Security, Kerberos, Group Managed Service Accounts, and related.

