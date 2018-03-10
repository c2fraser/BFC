---
layout: page
title: News
permalink: /news/
pagination:
  enabled: true
---
<div class="container"
<div id="index">
<h4>News</h4><BR>
{% for post in site.posts %}
     <article>
       {% if post.link %}
         <h4 class="link-post"><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a> <a href="{{ post.link }}" target="_blank" title="{{ post.title }}"><i class="fa fa-link"></i></a></h4>
       {% else %}
         <H5><a class="black-text" href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></H5>
         <H6 class="grey-text">{{ post.date | date: '%B %d, %Y' }}</h6>
         <p>{{ post.excerpt | strip_html | truncate: 250 }}</p>
         <hr class="style17"><br>
       {% endif %}
     </article>
   {% endfor %}
</div>
</div>
