---
layout: default
title: XieCraft
---
{% include JB/setup %}

{% for post in site.posts %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2> 
  <p class="author">
      {{ post.date | date: "%e %B, %Y"}}
  </p>
  <div class="content">
    {{ post.content }}
  </div>
{% endfor %}