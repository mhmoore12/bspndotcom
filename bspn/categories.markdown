---
layout: default
title: Categories
permalink: /categories/
---

<div class="categories-page">
    <h1>Categories</h1>
    <p>Explore all the categories available on BSPN to find the content that interests you the most. Click on any category to view all related articles.</p>

    <ul class="categories-list">
     {% for category in site.categories %}
      <li>
        <a href="/categories/{{ category[0] }}">{{ category[0] }}</a> ({{ category[1].size }})
      </li>
      {% endfor %}
    </ul>

</div>
