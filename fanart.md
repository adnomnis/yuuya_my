---
layout: masonry
permalink: fanart
---

{% assign fanart_posts = "" | split: "" %}
{% for post in site.posts %}
  {% if post.tag contains "fanart" %}
    {% assign fanart_posts = fanart_posts | push: post %}
  {% endif %}
{% endfor %}

<div id="masonry-grid" data-total="{{ fanart_posts.size }}" data-initial="10">
  {% for post in fanart_posts limit: 10 %}
    <div class="grid-item rkgk">
      <header class="time">{{ post.date | date: site.date_format }}</header>
      <div class="post-content">
        {{ post.content }}
      </div>
    </div>
  {% endfor %}
</div>