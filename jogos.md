---
layout: blog
title: "Análise de jogos"
permalink: /jogos/
---

<ul class="posts">
    {% for post in site.categories.jogos %}
        <li>
            <span class="post-date">{{ post.date | date: "%b %d, %Y" }}</span>
            :
            <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
        </li>
    {% endfor %}
</ul>
