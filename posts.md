---
layout: page
title: All Posts
permalink: /posts/
---

<div class="posts-archive">
  <h1>All Posts</h1>
  
  {%- if site.posts.size > 0 -%}
    <div class="posts-list">
      {%- for post in site.posts -%}
      <article class="post-entry">
        <div class="post-header">
          <h2>
            <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
          </h2>
          <p class="post-meta">
            <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: site.date_format }}</time>
            {%- if post.categories.size > 0 -%}
              <span class="post-categories">
                in 
                {%- for category in post.categories -%}
                  <span class="category">{{ category }}</span>
                  {%- unless forloop.last -%}, {%- endunless -%}
                {%- endfor -%}
              </span>
            {%- endif -%}
          </p>
        </div>
        
        {%- if post.excerpt -%}
          <div class="post-excerpt">
            {{ post.excerpt | strip_html | truncate: 200 }}
          </div>
        {%- endif -%}
        
        {%- if post.tags.size > 0 -%}
          <div class="post-tags">
            {%- for tag in post.tags -%}
              <span class="tag">{{ tag }}</span>
            {%- endfor -%}
          </div>
        {%- endif -%}
      </article>
      {%- endfor -%}
    </div>
  {%- else -%}
    <p>No posts yet.</p>
  {%- endif -%}
</div>

<style>
.posts-archive {
  max-width: 800px;
}

.posts-list {
  margin-top: 2rem;
}

.post-entry {
  margin-bottom: 2.5rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid var(--border-color, #eee);
}

.dark-theme .post-entry {
  border-bottom-color: #404040;
}

.post-entry:last-child {
  border-bottom: none;
}

.post-header h2 {
  margin: 0 0 0.5rem 0;
  font-size: 1.5rem;
}

.post-header h2 a {
  color: var(--text-color, #333);
  text-decoration: none;
}

.post-header h2 a:hover {
  color: var(--link-color, #2457c5);
}

.dark-theme .post-header h2 a {
  color: #e0e0e0;
}

.dark-theme .post-header h2 a:hover {
  color: #4a9eff;
}

.post-meta {
  color: var(--text-color-light, #666);
  font-size: 0.9rem;
  margin: 0;
}

.dark-theme .post-meta {
  color: #b0b0b0;
}

.post-categories {
  margin-left: 0.5rem;
}

.category {
  font-weight: 500;
}

.post-excerpt {
  margin: 1rem 0;
  line-height: 1.6;
  color: var(--text-color, #333);
}

.dark-theme .post-excerpt {
  color: #e0e0e0;
}

.post-tags {
  margin-top: 1rem;
}

.tag {
  display: inline-block;
  background-color: var(--surface-color, #f0f0f0);
  color: var(--text-color, #666);
  padding: 0.25rem 0.5rem;
  margin: 0 0.25rem 0.25rem 0;
  border-radius: 3px;
  font-size: 0.8rem;
}

.dark-theme .tag {
  background-color: #404040;
  color: #b0b0b0;
}
</style>
