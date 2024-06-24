---
permalink: /program
---

# Program

## Detailed program

Coming soon!

## List of provisionally accepted papers

<!-- Load all papers -->
{% assign papers = site.data.program.y2024.papers | sort: "title" %}

{% for paper in papers %}
{% include paper.html paper=paper %}
{% endfor %}