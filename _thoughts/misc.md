---
layout: page
title: Miscellaneous
description: A place for me to put writing that doesn't fit anywhere else.
order: 999
---

Basically the real blog on this website. Contains all of the stories and ideas that I
1. Wanted to write down and 
2. Didn't force myself to fit into a predefined category. 

Hopefully you enjoy, even if this page is always going to be a little disorganized.

### Posts
<!-- Do HTML/Liquid Magic -->
{%- assign posts = site.misc | sort: "date" -%}
<ul>
{%- for post in posts -%}
  <li><a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a> ({{post.englishdate}})</li>
{%- endfor -%}
</ul>