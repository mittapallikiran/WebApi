---
layout: default
---

For samples of ODataLib, EdmLib and .NET client for OData, visit [http://odata.github.io/odata.net/](http://odata.github.io/odata.net/).

{% for category in site.categories %} 
  <h2>{{ category[0] | join: "/" }}</h2>
  <ul>
  	{% for posts in category %}
      {% for post in posts reversed %}
      {% if post.url %} 
        <li><a href="{{site.baseurl}}{{ post.url }}">{{ post.title }}</a></li>
      {% endif %}
      {% endfor %}
    {% endfor %}
  </ul>
{% endfor %}