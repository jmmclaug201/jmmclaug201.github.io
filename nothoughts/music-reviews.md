---
layout: page
title: Music Reviews
description: A place for me to do my album reviews that isn't in front of my friends who've surely heard too many.
order: 2
---

Here, you'll find my reviews of various albums I've listened to, mostly from the 1960s and 1970s (At least eventually, as of now this very much in progress page is more of an album ranking than anything).

Please note I do not claim to be an actual music critic; these entries are mostly going to focus on my subjective opinions about different albums I've listened to (with a few random factoids thrown in). Hopefully you can find some enjoyment or use out of them nonetheless.

The albums are sorted by rating<!--, where I consider albums with titles in <span class=highlighter>color</span> to be particularly noteworthy-->.

<div class="album-list">
  {%- assign albums = site.albums | sort: "rating" | reverse -%}
  {%- assign i = 0 -%}
  {%- for upper in (1..10) reversed -%}
    {%- assign lower = upper | minus: 1 -%}
    <!-- Don't Print anything if no albums fit in bracket -->
    {%-if albums[i].rating<=lower or albums[i].rating > upper or i >= albums.size -%}
      {%- continue -%}
    {%-endif-%}
    <!-- Star Header for Rating Bracket -->
    {%- assign stars = upper | divided_by: 2 -%}
    {%- assign half = upper | modulo: 2 -%}
    <h3 style="color: gold">
      {%- for star in (1..stars) -%}★{%- endfor -%}
      {%- if half == 1 -%}½{%- endif -%}
    </h3>
    <!-- Print Albums in Bracket -->
    <ul style="margin: 0px">
    {%- for _ in site.albums -%}
      {%- if albums[i].rating<=lower or i >= albums.size -%}
        {%- break -%}
      {%- endif -%}
      {%- assign album = albums[i] -%}
      <a> <!-- href="{{ album.url | prepend: site.baseurl }}" -->
        <span class="album-entry">
        <div style="display: inline-block; padding: 0px 10px 0px;">
          {%- if album.album_cover -%}
            {%- include figure.html
              path=album.album_cover
              height=60
              width=60
              alt="" -%}
          {%- endif -%}
        </div>
          {%- if album.highlight == true -%}
            <span class="highlighter">{{album.title}}</span>
          {%- else -%}
            <span>{{album.title}}</span>
          {%- endif -%}
          <span style="color:black"> ({{album.artist}}, {{album.year}})</span> 
          <i style="color:gray">{{album.rating}}/10</i>
          </span>
        </a><br>
      {%- assign i = i | plus: 1 -%}
    {%- endfor -%}
    </ul>
  {%- endfor -%}
</div>


<!-- 
ALBUMS TO REVIEW:
 ***- Home and Away : Del Shannon

 **- The Doors : The Doors
 - Strange Days : The Doors
 - Waiting for the Sun : The Doors
 - The Soft Parade : The Doors
 - Morrison Hotel : The Doors
 *- L.A. Woman : The Doors

 **- Tommy : The Who
 - Live at Leeds : The Who
 *- Who's Next : The Who
 **- Quadrophenia : The Who
 - The Who By Numbers : The Who
 - Who Are You : The Who

 - A Hard Day's Night : The Beatles
 - Help! : The Beatles
 - Rubber Soul : The Beatles
 - Revolver : The Beatles
 - Sgt. Pepper's Lonely Heart's Club Band : The Beatles
 - Magical Mystery Tour : The Beatles
 - The White Album : The Beatles
 - Abbey Road : The Beatles

 *- Pet Sounds : The Beach Boys
 *- 20/20 : The Beach Boys

 *- How Great Thou Art : Elvis Presley
 **- Elvis NBC-TV Special : Elvis Presley
 **- From Elvis in Memphis : Elvis Presley
 *- From Memphis to Vegas/From Vegas to Memphis : Elvis Presley
 *- On Stage : Elvis Presley
 *- Almost In Love : Elvis Presley

 **- S.F. Sorrow : The Pretty Things

 - Mr. Tambourine Man : The Byrds
 - Turn! Turn! Turn! : The Byrds

 - The Velvet Underground : The Velvet Underground

 - All Things Must Pass : George Harrison

ALBUMS TO LISTEN TO:
 - Odyssey and Oracle : The Zombies
 - Forever Changes : Love
-->