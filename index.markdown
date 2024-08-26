---
layout: default
title: "Home"
---

<div class="hero-image">
    <div class="hero-text">
        <h2>Welcome to BSPN</h2>
        <p>Your source for all things Fantasy Footbug.</p>
    </div>
</div>

<div class="main-content">
    <section class="latest-articles">
        <h2 class="section-title">Latest Articles</h2>
 {% for post in site.posts limit:10 %}
    
    <article class="post">
            <header class="post-header">
                <h1 class="post-title"><a href="/bspn-site{{post.url}}">{{post.title}}</a></h1>
                <div class="post-meta">
                    <span class="author">Written by {{ post.author }}</span>
                    <span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
                </div>
            </header>
            <div class="post-content">
                <p class="excerpt">{{ post.excerpt }}</p>
            </div>
        </article>
  {% endfor %}

    </section>

    <aside class="sidebar">
        <h2 class="section-title">Categories</h2>
        <ul class="categories">
               {% for category in site.categories %}
      <li>
        <a href="/categories/{{ category[0] }}">{{ category[0] }}</a> ({{ category[1].size }})
      </li>
      {% endfor %}
        </ul>
    </aside>

</div>
