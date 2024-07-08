---
permalink: /program
---

# Program

<!-- Load all papers -->
{% assign papers = site.data.program.y2024.papers%}
{% assign sessions = site.data.program.y2024.sessions%}
{% assign keynote = site.data.program.y2024.keynote%}

Workshop location: [UCSC Hay Barn](https://cowellhaybarn.ucsc.edu/).  
See the [registration page](/register) for details.
{: .notice--primary}


## Breakfast

7:30 -- 8:20 (50min)
{: .notice}

## Workshop opening and awards

8:20 -- 8:30 (10min)
{: .notice}

<!-- Keynote -->
## Keynote: {{keynote.title}}

{{keynote.start}} -- {{keynote.stop}} ({{keynote.duration}})
{: .notice}

{% include keynote.html keynote=keynote %}

<!-- Paper sessions -->
{% for session in sessions %}
{%if session.id%}
## Session {{session.id}}: {{session.title}}
{%else%}
## {{session.title}}
{%endif%}

{{session.start}} -- {{session.stop}} ({{session.duration}})
{: .notice}

{% assign curr_session = session.id%}
{% include session.html session=curr_session papers=papers%}
{% endfor %}

<!-- Online papers -->
## Online program

Papers in the online program will **not** be presented during the workshop's live event.
{: .notice--primary}

{% include session.html session=99 papers=papers%}
