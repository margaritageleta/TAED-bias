---
title: "Welcome to our blog!"
---

Here is a list of all our posts available at the moment:
<ul>
  {% for post in site.posts %}
    <li>
      <a href="https://margaritageleta.github.io/TAED-bias/{{ post.url }}">{{ post.title }}</a><br/>
      {{ post.description }}
</li>
  {% endfor %}
</ul>
