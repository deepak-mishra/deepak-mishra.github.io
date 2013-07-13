---
layout: page
title: Deepak Mishra
tagline: Frontend Developer, UI Developer, Freelance web development, web design, graphic design!
---
{% include JB/setup %}
<article class="posts">
  {% for post in site.posts %}
    <h2> <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>  <em class="font12">{{ post.date | date_to_string }}</em></h2>
  {% endfor %}
</article>
