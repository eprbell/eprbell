---
layout: default
---

<div class="posts">
  {% for post in site.posts %}
    <div class="entry">
      <article class="post">

        <small>{{ post.date | date: "%B %e, %Y" }}</small>
        <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>

        {{ post.excerpt }}

        <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
      </article>
    </div>
  {% endfor %}
</div>