---
title: "Welcome to our blog!"
---
We are happy to announce that we have finally published an Open Repository for Machine Translation DataSheets! **[Check it out!](https://mtdatasheets.cs.upc.edu)**

Here is a list of all our posts available at the moment:
<ul>
  {% for post in site.posts reversed %}
    <li>
      <a href="{{margaritageleta.github.io}}{{site.baseurl}}{{post.permalink}}">{{post.title}}</a><br/>
      {{ post.description }}
  </li>
    {% if {{post.image}} != null %}
    <div style="width: 100%; height:200px; display:flex; justify-content: center; align-items: center; margin-top: 15px; margin-bottom: 15px;">  
      <div style="background-image: url('{{post.image}}'); height:100%; width:80%; background-repeat: no-repeat; background-size: cover;"></div>
    </div>
    {% endif %}
  {% endfor %}
</ul>
