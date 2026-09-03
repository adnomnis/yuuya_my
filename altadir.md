---
layout: masonry
permalink: oc
---

<div id="masonry-grid">
  {% for post in site.posts %}
    {% if post.tag contains "altadir" %}
      <div class="grid-item rkgk">
        <header class="time">{{ post.date | date: site.date_format }}</header>
        <div class="post-content">
          {{ post.content }}
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>