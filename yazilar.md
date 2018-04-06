---
layout: page
title: "Emre Dündar"
subtitle: "açık not defteri"
css: "/css/index.css"
meta-title: "Emre Dündar - Açık Not Defteri"
meta-description: " "
---

<div class="list-filters">
  <a href="/" class="list-filter">TR</a>
  <span class="list-filter filter-selected">TR</span>
  <a href="/posts" class="list-filter">EN</a>
</div>

<div class="posts-list">
  {% for post in site.tags.tr %}
  <article>
    <a class="post-preview" href="{{ post.url | prepend: site.baseurl }}">
	    <h2 class="post-title">{{ post.title }}</h2>
	
	    {% if post.subtitle %}
	    <h3 class="post-subtitle">
	      {{ post.subtitle }}
	    </h3>
	    {% endif %}
      <p class="post-meta">
        Posted on {{ post.date | date: "%B %-d, %Y" }}
      </p>

      <div class="post-entry">
        {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
        <span href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</span>
      </div>
    </a>  
   </article>
  {% endfor %}
</div>
