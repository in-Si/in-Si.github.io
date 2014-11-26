---
permalink:    /by_language/
layout:      	pages
title:     		Apps by language
---

<div class="home">

<ol id="page-top">
{% for lang in site.languages %}
  <li><a class="page-scroll" href="#{{lang}}">{{lang}}</a></li>
{% endfor %}
</ol>

<hr>

{% for lang in site.languages %}
  <h3 id="{{lang}}">{{lang}}</h3>
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
  <a class="page-scroll" href="#page-top">Back to language list</a>
  <hr>
{% endfor %}

</div>
