---
layout: post
title: empty category 2
---
<p>
page.category
{{ page.category }}
</p>
<p>
page.category | inspect
{{ page.category | inspect }}
</p>
<br>
{% if page.categories == empty %}
    > no!!!
{% endif %}

{% for post in site.posts %}
{% if post.categories == empty %}
{{ post.title }}
{% endif %}
{% endfor %}
