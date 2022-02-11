---
layout: page
title: Interests
permalink: /interests/
---

{% for category in site.categories %}
{% if category[0] == "interests" %}
  <div>
    {% for post in category[1] %}
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}" style="color:gray; font-size:90%;" >{{ post.date | date_to_long_string }}</time>
    <h3><a href="{{ post.url }}"> {{ post.title }}</a></h3>
    {% endfor %}
  </div>
{% endif %}
{% endfor %}

<!-- <h2>{{ category[0] }}</h2> -->
<!-- <li><a href="{{ post.url }}">{{ post.title }}</a></li> -->
