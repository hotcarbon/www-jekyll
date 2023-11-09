---
permalink: /read
# toc: false
classes: wide
---

# 2nd Edition - 2023

<!-- Loop through all papers -->
{% assign papers = site.data.program.y2023.papers %}
{% for paper in papers %}
{% include paper.html 
    title=paper.title 
    authors=paper.authors 
    pdf=paper.pdf
    video=paper.video
    yt-id=paper.yt-id
%}
{% endfor %}<!-- Loop through all papers -->


# 1st Edition - 2022

<!-- Loop through all papers -->
{% assign papers = site.data.program.y2022.papers %}
{% for paper in papers %}
{% include paper.html 
    title=paper.title 
    authors=paper.authors 
    pdf=paper.pdf
    video=paper.video
    yt-id=paper.yt-id
%}
{% endfor %}<!-- Loop through all papers -->