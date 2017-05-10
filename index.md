---
layout: page
title: Blog
tagline: Tagline Content
---
{% include JB/setup %}
    
<ul class="posts">
  {% for post in site.posts %}
    <li>
		<span>{{ post.date | date_to_string }}</span> &raquo; 
		<a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
		{% if post.excerpt_tag %}
          {{ post.excerpt_tag | markdownify }}
          <a href="{{ post.url | prepend: site.baseurl }}">Read more...</a>
        {% else %}
          {{ post.content }}
        {% endif %}
	</li>
  {% endfor %}
</ul>
