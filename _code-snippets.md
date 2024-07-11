
# News list
{% for post in site.posts limit:include.n-item %}
<div class="notice">  
<!-- <div style="display: inline-block; width: 25%; vertical-align: top;"> -->
    <p>{{ post.date | date: "%b. %-d, %Y" }}</p>
<!-- </div><div style="display: inline-block; width: 75%; vertical-align: top;"> -->
    <p><strong>{{ post.title }}</strong></p>
    {{ post.content }}
</div>
<!-- </div> -->
{% endfor %}


## List of provisionally accepted papers

<!-- Load all papers -->
{% assign papers = site.data.program.y2024.papers | sort: "title" %}

{% for paper in papers %}
{% include paper.html paper=paper %}
{% endfor %}


# Latest publications

{% bibliography --max 3 --sort %}
<br>


  <!-- Embeded video -->
  {% if include.paper.yt-id %}
  {% capture youtube-id %}{{include.paper.yt-id}}{% endcapture %}
  {% include video id=youtube-id provider="youtube" %}
  {% endif %}

# Latest News
<ul class="post-list">
  {% for post in site.posts limit:1 %}
  {% if post.type == "news" %}
  <li>
    <h4>{{ post.title }}
    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span></h4>
    {{ post.content }}
  </li>
  {% endif %}
  {% endfor %}
</ul>


<!-- Loop through all members of one area -->
<!-- {% assign members = site.data.areas.students.board | sort: "name" %} -->
<!-- {% for member in members %} -->
<!-- - [{{member.name}}]({{member.webpage}}), {{member.affiliation}}{% endfor %} -->

