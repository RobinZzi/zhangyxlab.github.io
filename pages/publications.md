---
layout: page-fullwidth
title: "Publications"
permalink: "/publications/"
---
<a href="https://scholar.google.com/citations?hl=en&user=XU7ZT5kAAAAJ"> For a complete list of Bing Ren's publications, click here.</a>

<ul>
  {% for post in site.categories.publication %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> 
     <br> {{post.pub.authors}} <br>
      <b> {{post.pub.journal}}</b>, {{post.pub.date}},
    </li>
  {% endfor %}
</ul>
