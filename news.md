---
layout: page
title: News
permalink: /news/
pagination:
  enabled: true
---
<div class="container">
<div id="index">
<h4>News</h4><BR>
{% for post in site.posts %}
     <article>
       {% if post.link %}
         <h4 class="link-post"><a href="{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a> <a href="{{ post.link }}" target="_blank" title="{{ post.title }}"><i class="fa fa-link"></i></a></h4>
       {% else %}
         <H6 class="line" style="font-weight: bold;"><a class="black-text" href="{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></H6>
         <p class="news-date">{{ post.date | date: '%B %d, %Y' }}</p>
         <p>{{ post.excerpt | strip_html | truncate: 250 }}</p>
         <hr class="style17"><br>
       {% endif %}
     </article>
   {% endfor %}
</div>
</div>
