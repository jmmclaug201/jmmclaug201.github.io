---
layout: page
permalink: /thoughts/
title: thoughts
pagetitle: A Directory of Thoughts<sup>1</sup>
description:
nav: true
nav_order: 1
---

As per the title, this page serves as a place to find all of my writing that I didn't feel was important enough for the main page, organized by topic. 

  <ul class="thought-list">
    <hr class="blog-hr"/>
    {% for thought in site.thoughts %}
      <h3>
        {% if thought.redirect == blank %}
          <a class="post-title" href="{{ thought.url | prepend: site.baseurl }}">{{ thought.title }}</a>
        {% else %}
            <a class="post-title" href="{{ thought.redirect | relative_url }}">{{ thought.title }}</a>
        {% endif %}
      </h3>
      <p>{{ thought.description }}</p>
      <hr class="blog-hr"/>
    {% endfor %}
  </ul>


<sup>1</sup> I considered naming this page "blogs", but felt it was far too pretentious to say I needed multiple blogs while other people's musings fit in one.