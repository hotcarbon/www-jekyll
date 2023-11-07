---
permalink: /read
toc: true
---

<!-- Loop through all papers -->
{% assign papers = site.data.program.y2022.papers %}
{% for paper in papers %}
{{paper.title}}
{{paper.authors}}
{% endfor %}<!-- Loop through all papers -->

# Volume 3 (2023)

{% bibliography --query @*[volume=3] %}


# Volume 2 (2022)

{% bibliography --query @*[volume=2] %}


# Volume 1 (2021)

{% bibliography --query @*[volume=1] %}
