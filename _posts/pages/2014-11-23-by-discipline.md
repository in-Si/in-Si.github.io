---
permalink:    /by_discipline/
layout:        pages
title:     		Apps by discipline
---

<div class="home">

<ol id="page-top">
{% for disc in site.disciplines %}
  <li><a class="page-scroll" href="#{{disc}}">{{disc}}</a></li>
{% endfor %}
</ol>

<hr>

{% for disc in site.disciplines %}
  <h3 id="{{disc}}">{{disc}}</h3>
  <table class="list_apps">
    {% for post in site.posts %}
      {% for tag in post.tags %}
        {% if tag == disc %}
          <tr> 
            <td><a href="{{ post.url }}"><img class="img_apps_thumb" src="{{ post.image }}"></a></td>
            <td>{{ post.excerpt }}</td>
          </tr>
        {% endif %}
      {% endfor %}
    {% endfor %}
  </table>
  <a class="page-scroll" href="#page-top">Back to discipline list</a>
  <hr>
{% endfor %}

</div>
