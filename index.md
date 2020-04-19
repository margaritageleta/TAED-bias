---
title: "Welcome to our blog!"
---

Here is a list of all our posts available at the moment:
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{margaritageleta.github.io}}{{site.baseurl}}{{post.permalink}}">{{post.title}}</a><br/>
      {{ post.description }}
</li>
  {% endfor %}
</ul>
