---
layout: blog
title: "Lista de categorias"
permalink: /categorias/
---

<header>
    <h1>Categorias</h1>
</header>

<ul class="tag-box inline">
{% assign list = site.tags | sort %}
    {% for categoria in list %} 
        <li>
            <a href="#{{ categoria[0] }}">
                {{ categoria[0] }}
            </a>
            <span>({{ categoria[1].size }})</span>
        </li>
    {% endfor %}
{% assign list = nil %}
</ul>

{% assign taglist = site.tags | sort %}
{% for categoria in taglist %} 
 <h2 id="{{ categoria[0] }}">{{ categoria[0] }}</h2>
 <ul class="post-list">
  {% assign list = categoria[1] %}  
  {% for post in list %}
   <li>
   <a href="{{ post.url }}">{{ post.title }}</a>
   </li>
  {% endfor %}
  {% assign pages_list = nil %}
  {% assign group = nil %}
 </ul>
{% endfor %}
{% assign taglist = nil %}
