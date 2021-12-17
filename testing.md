---
title: Testing Jekyll constructs
customSpecialVarb: Pizza
---

{{ site.plugins | inspect }}

{% assign about_me = site.pages | where:"name","readme.md" | first %}
## {{ about_me.url | split: '/' | last | split: '.' | first }} me
{{ about_me.excerpt | default: about_me.content | split: site.excerpt_separator | first }}

cover letter notes: 
 - length: 250-400 words long
 - Header - Input contact information
 - Greeting the hiring manager
 - Opening paragraph - Grab the reader’s attention with 2-3 of your top achievements
 - Second paragraph - Explain why you’re the perfect candidate for the job
 - Third paragraph - Explain why you’re a good match for the company
 - Formal closing


- IP phones count as devices
- So do cameras
- So do iPhones
- medical equipment!

