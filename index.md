---
layout: default
title: Chi Kung Stories
---
<div class='post'>
    <div class='body'>
   {% for post in site.posts limit:1 %}
      	<h2>{{post.title}}</h2>
      	{{ post.content }}
    {% endfor %}
    </div>
</div>


