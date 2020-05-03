---
title: "Welcome to our blog!"
---

Here is a list of all our posts available at the moment:
<ul>
  {% for post in site.posts reversed %}
    <li>
      <a href="{{margaritageleta.github.io}}{{site.baseurl}}{{post.permalink}}">{{post.title}}</a><br/>
      {{ post.description }}
  </li>
  <div style="width: 100%; height:50px; display:flex; justify-content: center; align-items: center;">  
    <div style="background-image: url('{{post.image}}'); height:100%; width:50%;"></div>
  </div>
  {% endfor %}
</ul>
