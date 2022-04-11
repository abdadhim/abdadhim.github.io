---
layout: page
title: Projects
permalink: /projects/
---

{% for category in site.categories %}
{% if category[0] == "projects" %}
  <div>
    {% for post in category[1] %}
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}" style="color:gray; font-size:90%;" >{{ post.date | date_to_long_string }}</time>
        {% if post.title contains "[Work-In-Progess]" %}
        <h3><a href="{{ post.url }}" style="color:#C3C3C3;"> {{ post.title }}</a></h3>
        {% else %}
        <h3><a href="{{ post.url }}"> {{ post.title }}</a></h3>
        {% endif %}
    
    {% endfor %}
  </div>
{% endif %}
{% endfor %}
