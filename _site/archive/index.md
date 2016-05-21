
---
Layout: page
title: Archive
---

<script src="/js/lunr.min.js"></script>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
<script src="/js/search.js"></script>

<form action="get" id="site_search">
  <label for="search_box">Search</label><input type="text" id="search_box">
  <input type="submit" value="search">
</form>

<ul id="search_results"></ul>
<ul>
{% for post in site.posts %}
  <li>
    {{ post.date | date: "%b %d, %Y"  }} &mdash; <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
