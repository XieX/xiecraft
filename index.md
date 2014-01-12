---
layout: default
title: XieCraft
---
{% include JB/setup %}

<div class='panel-housing' style='margin-left: auto; margin-right: auto; width: 95%; text-align: center;'>
{% for post in site.posts %}
  <div class='panel-outer' style='display: inline-block; vertical-align: top; padding: 10px; width: 300px; zoom: 1; *display: inline;'>
    <div class='panel-inner' style='width: 85%; background-color: #f5f5f5; padding: 10px;'>
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3> 
        <p class="author">
          {{ post.date | date: "%e %B, %Y"}}
        </p>
        <p>
          {% if post.thumbnail %}
            <img src='{{ post.thumbnail }}' width='75%' />
          {% endif %}
        </p>
        <div style="text-align:justify;">
          {{ post.content | more: 'excerpt' }}
        </div>
        <div style="font-size: large; text-align: right;">
          <a href="{{ post.url }}">Read more...</a>
        </div>
      </div>
  </div>
{% endfor %}
</div>