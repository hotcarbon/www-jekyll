---
permalink: /program
---

# Program

Condensed program as [PDF](/assets/2025/program.pdf)
{: .notice--warning}

<!-- Load all papers -->
{% assign papers = site.data.program.y2025.papers%}
{% assign sessions = site.data.program.y2025.sessions%}
{% assign keynote = site.data.program.y2025.keynote%}
{% assign keynote2 = site.data.program.y2025.keynote2%}

## Day 1 - Thursday, July 10, 2025

{% for session in sessions %}
{%if session.day == 1%}
{%if session.id and session.id == 'keynote'%}
### Keynote: {{keynote.title}}
{{keynote.start}} -- {{keynote.stop}} ({{keynote.duration}})
{: .notice}
{% include keynote.html keynote=keynote %}
{%else%}
{% assign curr_session = session.id%}
{% include session.html session=curr_session papers=papers%}
{%endif%}
{%endif%}
{% endfor %}


## Day 2 - Friday, July 11, 2025

{% for session in sessions %}
{%if session.day == 2%}
{%if session.id and session.id == 'keynote'%}
### Keynote: {{keynote2.title}}
{{keynote.start}} -- {{keynote.stop}} ({{keynote.duration}})
{: .notice}
{% include keynote.html keynote=keynote2 %}
{%else%}
{% assign curr_session = session.id%}
{% include session.html session=curr_session papers=papers%}
{%endif%}
{%endif%}
{% endfor %}


<!-- Online papers -->
<!-- ## Online program

Papers in the online program will **not** be presented during the workshop's live event.
{: .notice--primary}

{% include session.html session=99 papers=papers%} -->