---
layout: default
---

<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      {{ moment().format('YYYY-MM-DD HH:m:s'); post.date }}
      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>