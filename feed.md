---
title: Feed
layout: default
published: false
---
<h3 style="text-align:center;color:#9AF777;padding-top:15px;font-size:18px">All Posts</h3>
<div class="home">

  {% assign posts = site.posts %}

  {%- if posts.size > 0 -%}
    {%- if page.list_title -%}
      <h1 class="post-list-heading">{{ page.list_title }}</h1>
    {%- endif -%}
    <div class="box home-box">
      <div class="post-list">
        {%- for post in posts -%}

          <a class="post-link" style="text-align:center" href="{{ post.url | relative_url }}">
            <h1 style="font-size:22px">{{ post.title | escape }}</h1>
          {%- if post.image -%}
            <div style="text-align:center">
              <img src=" {{ post.image }}" width="200px" >
            </div>
          {%- endif -%}
          </a>

        {%- endfor -%}
      </div>
    </div>
  {%- endif -%}

</div>