---
title: "Tags"
permalink: /tags/
layout: tags
author_profile: true
---

---
layout: default
title: Directorio de Etiquetas
---

<h1>Todas las etiquetas</h1>


{% assign all_tags = site.tags %}

{% for item in site.portafolio %}
    {% for tag in item.tags %}
        {% assign all_tags = all_tags | push: tag %}
    {% endfor %}
{% endfor %}


{% for game in site.games %}
    {% for tag in game.tags %}
        {% assign all_tags = all_tags | push: tag %}
    {% endfor %}
{% endfor %}


{% assign unique_tags = all_tags | uniq | sort %}


{% for tag in unique_tags %}
    <h2 id="{{ tag | slugify }}">{{ tag }}</h2>

    <ul>
        <!-- Mostramos posts con esta etiqueta -->
        {% for post in site.posts %}
            {% if post.tags contains tag %}
                <li><strong>[Post]</strong> <a href="{{ post.url }}">{{ post.title }}</a></li>
            {% endif %}
        {% endfor %}

        <!-- Mostramos items del portafolio con esta etiqueta -->
        {% for item in site.portafolio %}
            {% if item.tags contains tag %}
                <li><strong>[Portafolio]</strong> <a href="{{ item.url }}">{{ item.title }}</a></li>
            {% endif %}
        {% endfor %}

        <!-- Mostramos games con esta etiqueta -->
        {% for game in site.games %}
            {% if game.tags contains tag %}
                <li><strong>[Game]</strong> <a href="{{ game.url }}">{{ game.title }}</a></li>
            {% endif %}
        {% endfor %}
    </ul>
{% endfor %}