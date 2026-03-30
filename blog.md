---
layout: vanilla
title: blog
---

## my blog
thanks for checking out my blog! i like to write about anything that comes to mind!

you're only shown a snippet of the post, so make sure to click on the post if you want to read the whole thing!

---

<ul class="post_ul">
  {% for post in site.posts %}
  <a href="{{ post.url }}" class="a_blog">
    <div class="div_blog">
      <li class="post_li">
        <h3>{{ post.title }}</h3>
        <h4>{{ post.date | date_to_string }}</h4>
        <div class="excerpt_SHOW">{{ post.excerpt }}</div> <strong>... click to read more!</strong>
      </li>
    </div>
  </a>
  {% endfor %}
</ul>
