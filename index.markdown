---
layout: wrapper
---

{% for post in site.posts %}

{% if post.tag contains "status" %}

<div class="status">

<header class="time">{{ post.date | date: site.date_format }}</header>
{{ post.content }}
</div>

{% endif %}

{% endfor %}