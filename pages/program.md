---
permalink: /program
# toc: false
toc: true
---

# Program

<!-- Condensed program as [PDF](/assets/2025/program.pdf)
{: .notice--warning} -->

<!-- HotCarbon will be back in 2026!   -->
<!-- You can find the papers of past editions in their respective pages (see left panel). -->
<!-- {: .notice--warning} -->


<!-- Load all papers -->
{% assign papers = site.data.program.y2026.papers%}
{% assign sessions = site.data.program.y2026.sessions%}
{% assign keynote = site.data.program.y2026.keynote%}
{% assign keynote2 = site.data.program.y2026.keynote2%}

## Day 1 - Thursday, July 16, 2026

{% for session in sessions %}
{%if session.day == 1%}
{%if session.id and session.id == 'keynote'%}
### Keynote: {{keynote.title}}
<!-- {{keynote.start}} -- {{keynote.stop}} ({{keynote.duration}})
{: .notice} -->
{% include keynote.html keynote=keynote %}
{%else%}
{% assign curr_session = session.id%}
{% include session.html session=curr_session papers=papers%}
{%endif%}
{%endif%}
{% endfor %}


## Day 2 - Friday, July 17, 2026

{% for session in sessions %}
{%if session.day == 2%}
{%if session.id and session.id == 'keynote'%}
### Keynote: {{keynote2.title}}
<!-- {{keynote.start}} -- {{keynote.stop}} ({{keynote.duration}})
{: .notice} -->
{% include keynote.html keynote=keynote2 %}
{%else%}
{% assign curr_session = session.id%}
{% include session.html session=curr_session papers=papers%}
{%endif%}
{%endif%}
{% endfor %}

