---
layout: default
---

<div class="posts">
  {% for post in site.posts %}
    <p>
    <article class="post">

      <small>{{ post.date | date: "%e %B, %Y" }}</small>
      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
    </p>
  {% endfor %}
</div>