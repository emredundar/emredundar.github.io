---
layout: page
title: "Emre Dündar"
subtitle: personal website
css: "/css/index.css"
meta-title: "Emre Dündar - Posts in English"
meta-description: " "
---

<div class="list-filters">
  <a href="/" class="list-filter">All posts</a>
  <a href="/tr" class="list-filter">TR</a>
  <span class="list-filter filter-selected">EN</span>
</div>

<div class="posts-list">
  {% for post in site.tags.en %}
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
