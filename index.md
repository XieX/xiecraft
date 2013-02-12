---
layout: default
title: XieCraft
---
{% include JB/setup %}

{% assign close_off = false %}

<table cellpadding="10">
  {% for post in site.posts %}
    {% cycle '<tr>', '' %}
      <td width="50%">
        <div style='{% cycle 'background: grey;', 'background: blue;' %} margin-left: auto; margin-right: auto; width: 95%; text-align: center;'>
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2> 
        <p class="author">
          {{ post.date | date: "%e %B, %Y"}}
        </p>
        <p>
          {% if post.thumbnail %}
            <img src='{{ post.thumbnail }}' width='75%' />
          {% else %}
            <img src='/assets/img/xiewtfface.jpeg' width='75%' />
          {% endif %}
        </p>
        </div>
        <div style="text-align:justify;">
          {{ post.content | more: 'excerpt' }}
        </div>
        <div style="font-size: large; text-align: right;">
          <a href="{{ post.url }}">Read more...</a>
        </div>
      </td>
    {% cycle '', '</tr>' %}

    {% if close_off %}
      {% assign close_off = false %}
    {% else %}
      {% assign close_off = true %}
    {% endif %}
  {% endfor %}

  {% if close_off %}
    </tr>
  {% endif %}
</table>