---
layout: page
title: Categorias
permalink: /categorias/
---
<ul>
{% raw %}{% for c in site.categories %}
<li><a href="#{{ c[0] | slugify }}">{{ c[0] }}</a> ({{ c[1] | size }})</li>
{% endfor %}{% endraw %}
</ul>


{% raw %}{% for c in site.categories %}
<h2 id="{{ c[0] | slugify }}">{{ c[0] }}</h2>
<ul>
{% for post in c[1] %}
<li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> <small>({{ post.date | date_to_string }})</small></li>
{% endfor %}
</ul>
{% endfor %}{% endraw %}
