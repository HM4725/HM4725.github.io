---
layout: default
---
<ul class="posts-list">
  {% for post in site.posts %}
    {% if post.categories == empty %}
    <li>
      <h3>
        <a href="{{ site.baseurl }}{{ post.url }}">
          {{ post.title }}
        </a>
        <small>{{ post.date | date_to_string }}</small>
      </h3>
    </li>
    {% endif %}
  {% endfor %}
</ul>
