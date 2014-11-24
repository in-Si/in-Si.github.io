---
permalink:    /by_language/
layout:      	pages
title:     		Apps by language
---

<div class="home">

{% for lang in site.languages %}
  <h3>{{lang}}</h3>
  <table class="list_apps">
    {% for post in site.posts %}
      {% for tag in post.tags %}
        {% if tag == lang %}
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


