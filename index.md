---
layout: home
title: Home
nav_order: 1
seo:
  type: Course
  name: Linux Sysadmin Decal
---

# {{ site.tagline }}
{: .mb-2 }
{{ site.description }}
{: .fs-6 .fw-300 }

{% if site.announcements %}
{{ site.announcements.last }}
[Announcements](announcements.md){: .btn .btn-outline .fs-3 }
{% endif %}

## Weekly Schedule
{% for schedule in site.schedules %}
{{ schedule }}
{% endfor %}

# Calendar

<div class="module" markdown="1">
## Week 0: 8/30/2021
{: .text-gamma }

Infosession
: **Infosession**{: .label .label-yellow}[ocf.io/decalzoom](https://ocf.io/decalzoom)
: **Lab**{: .label .label-yellow}[Lab 0](https://docs.google.com/forms/u/3/d/1pTDvGX2f6eB2zoTSv757TWVvjFBa1jFCX25Y5hZTH2A/edit)
    : **Lab due Sat. 1/29**
</div>
{% for week in site.data.materials %}
<div class="module" markdown="1">
## Week {{week.id}}: {{week.date}}
{: .text-gamma }

{% if week.hidelink %}
Beginner Track
: **Lecture**{: .label .label-green}{{week.beginner-name}}
: **Lab**{: .label .label-blue}Lab b{{week.id}}
    : **Lab due {{week.labdue}}**

Advanced Track
: **Lecture**{: .label .label-purple }{{week.advanced-name}}
: **Lab**{: .label .label-red}Lab a{{week.id}}
    : **Lab due {{week.labdue}}**
    
{% elsif week.beginner-solutions %}
Beginner Track
: **Lecture**{: .label .label-green}[{{week.beginner-name}}]({{week.beginner-video}}) 
    : [Slides]({{week.beginner-slides}}){:target="_blank"}
: **Lab**{: .label .label-blue}[Lab b{{week.id}}](labs/b{{week.id}}) &nbsp; &nbsp; [(Solution)]({{week.beginner-solutions}})
    : **Lab due {{week.labdue}}**

Advanced Track
: **Lecture**{: .label .label-purple }[{{week.advanced-name}}]({{week.advanced-video}})
    : [Slides]({{week.advanced-slides}}){:target="_blank"}
: **Lab**{: .label .label-red}[Lab a{{week.id}}](labs/a{{week.id}}) &nbsp; &nbsp; [(Solution)]({{week.advanced-solutions}})
    : **Lab due {{week.labdue}}**
{% else %}
Beginner Track
: **Lecture**{: .label .label-green}[{{week.beginner-name}}]({{week.beginner-video}}) 
    : [Slides]({{week.beginner-slides}})
: **Lab**{: .label .label-blue}[Lab b{{week.id}}](labs/b{{week.id}})
    : **Lab due {{week.labdue}}**

Advanced Track
: **Lecture**{: .label .label-purple }[{{week.advanced-name}}]({{week.advanced-video}})
    : [Slides]({{week.advanced-slides}}){:target="_blank"}
: **Lab**{: .label .label-red}[Lab a{{week.id}}](labs/a{{week.id}})
    : **Lab due {{week.labdue}}**
{% endif %}
</div>
{% endfor %}

<div class="module" markdown="1">
## Week 11
{: .text-gamma }
Extra Lab! (Optional)
: **Lab**{: .label .label-yellow} [Lab 11](labs/11)
    : **Lab due Sun. 5/7**
</div>
