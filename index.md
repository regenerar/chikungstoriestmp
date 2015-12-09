---
layout: default
title: Chi Kung Stories
---
<div class='post'>
    <div class='body'>
   {% for post in site.posts limit:1 %}
      	<h2>{{post.title}}</h2>
		<article>
      {% if post.image %}
        <p align="center"><img src="{{ base.url }}{{ post.image }}" style="border-radius: 15px; width: 100%"></p>
      {% endif %}

      	{{ post.content }}
      </article>

      {% if post.video %}
        <iframe src="https://player.vimeo.com/video/{{ post.video }}" width="720" height="406" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

        <p><a href="{{ post.video-url }}">Chi kung Stories Home Practice Video</a> from <a href="https://vimeo.com/user44749248">Lourenco de Azevedo</a></p>

      {% endif %}

      {% if post.file %}
        <audio src="{{ post.file }}" preload="none" controls="controls" type="audio/mp3">
        Your browser doesn't support the <code>audio</code> element.
        </audio>
        <br>
        <a href="{{ post.file }}" class="button">Download podcast</a>
      {% endif %}
           	
    {% endfor %}
    </div>
</div>


