---
layout: page
title: Archive
---

<script src="/js/lunr.min.js"></script>
<script src="/js/jquery.min.js"></script>
<script src="/js/search.js"></script>
<style type="text/css">
#search_box{
  border:2px solid black;
  border-radius: 90px;
  padding:0.5em 1em;
}
#search_button {
  display: none;
}
</style>
<form action="get" id="site_search">
  <label for="search_box">Search  </label><input type="text" id="search_box">
  <input type="submit" value="search" id="search_button">
</form>

<ul id="search_results"></ul>
<ul>
{% for post in site.posts %}
  <li>
    {{ post.date | date: "%b %d, %Y"  }} &mdash; <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
