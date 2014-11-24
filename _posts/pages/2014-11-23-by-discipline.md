---
permalink:    /by_discipline/
layout:        pages
title:     		Apps by discipline
---

<div class="home">

{% for disc in site.disciplines %}
  <h3>{{disc}}</h3>
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
{% endfor %}

</div>


