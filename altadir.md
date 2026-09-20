---
layout: masonry
permalink: altadir
---

{% assign altadir_posts = "" | split: "" %}
{% for post in site.posts %}
  {% if post.tag contains "altadir" %}
    {% assign altadir_posts = altadir_posts | push: post %}
  {% endif %}
{% endfor %}

<div id="masonry-grid" data-total="{{ altadir_posts.size }}" data-initial="10">
  {% for post in altadir_posts limit: 10 %}
    <div class="grid-item rkgk">
      <header class="time">{{ post.date | date: site.date_format }}</header>
      <div class="post-content">
        {{ post.content }}
      </div>
    </div>
  {% endfor %}
</div>