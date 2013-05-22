---
layout: country
title: Welcome to the Mexico project pages
description: A comprehensive list of indexing projects in Mexico
categories: none
---

<h1>Main Project Page for Mexico</h1>

<div class="right">
  <h2 class="no-top-border">Pages: </h2>
  <div id="pages">
    <ul>
      {% for page in site.html_pages %}
        {% if page.title %}
            <li><a href="{{ page.url | remove:'index.html' }}">{{ page.title }}</a></li>
        {% endif %}
      {% endfor %}
    </ul>
  </div>

  <h2>Posts:</h2>
  <div id="posts">
    <ul>
      {% for post in site.categories.blog %}
        <li><a href="{{ post.url }}/">{{ post.title }}</a><br/><span class="blogpostdate">{{ post.date | date_to_string }}</span></li>
      {% endfor %}
    </ul>
  </div>
</div>
