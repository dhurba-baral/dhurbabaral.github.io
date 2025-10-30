---
layout: page
title: Blogs
subtitle: Recent posts and notes
permalink: /blogs/
---

Welcome! Below are recent posts.

<div class="post-list">
  {% for post in site.posts %}
    <div class="post-entry">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <div class="entry-date">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: site.date_format | default: "%B %-d, %Y" }}</time>
      </div>
      {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | truncate: 140 }}</p>
      {% endif %}
    </div>
  {% endfor %}
</div>


