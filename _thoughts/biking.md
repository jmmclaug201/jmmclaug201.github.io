---
layout: page
title: Biking
description: Biking things and ride reports.
order: 1
---

> "Twelve miles an hour is about the perfect speed for a human to travel"
> 
> [\- Paul Suchecki](https://www.youtube.com/@paulsuchecki3985)

Here, you'll find all of my posts related to biking, which I find myself doing a lot these days. 

### Links
Some places I find myself coming back to whenever I need biking inspiration:
- [Eric Zheng's Cycling Blog](https://ericzheng.org/cycling/index.html), which I often read for ride ideas and which I ~~copied~~ was heavily inspired by in creating this blog.
- [Komoot](https://www.komoot.com/plan), my go-to ride planning site.
- [Waymarked Trails](https://cycling.waymarkedtrails.org/#?map=10.0/40.4344/-79.9103), a comprehensive OpenStreetMap-based map of bike trails and routes.
- Some Youtube Channels I like for motivation:
  - [Paul Suchecki](https://www.youtube.com/@paulsuchecki3985), who I especially like for his down-to-earth style as he bikes different trails around the United States.
  - [Ryan Van Duzer](https://www.youtube.com/channel/UCVcUzl95VwxrIEQnu9xI21g), and especially his video on [different biking routes across the United States](https://www.youtube.com/watch?v=T8LB1gYzyVo).
- Some resources for biking around Pittsburgh:
  - A [comprehensive book](https://www.cs.cmu.edu/~apd/Pittsburgh/Oscar_Swan_Bike_Rides_Out_of_Pittsburgh.pdf) of local routes (which I found via Eric Zheng's blog).
  - A [website](https://www.cs.cmu.edu/afs/cs/user/spok/bike/#doortodoor) with a bunch of links to various resources for biking in the area.
  - [BikePGH](https://bikepgh.org/), the local cycling organization.

### Ride Reports
Some posts I've written about rides I'm particularly fond of. All of the posts has an associated [komoot](https://www.komoot.com/user/2743683532488) activity if you want to see the route in more detail. Any <span class="highlighter">highlighted</span> rides are personal favorites of mine.

I also have a bit of a backlog of rides to write about, so bear with me as I get that done in what will hopefully be a reasonable timeframe.

<!-- To Make
  Butler-Freeport Ride
  Tri-State Century ***
  Orient Point
  Fake Boston Woods
  Atom Smasher
  Great Allegheny Passage ***
  Dravo Cemetery
  East Coast Greenway
  First ride around Shelter Island-->

{%- assign posts = site.bike-ride-reports | sort: "date" | where: "unfinished", nil | reverse -%}
<ul>
{%- for post in posts -%}
  {%- if post.highlight -%}
    <li><span class="highlighter">
    <a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a></span> - {{post.date | date: "%B %-d, %Y"}}</li>
  {%- else -%}
    <li>
    <a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a> - {{post.date | date: "%B %-d, %Y"}}</li>
  {%- endif -%}
{%- endfor -%}
</ul>

### Other Pages
Finally, some other biking-related posts I've written that aren't ride reports:

<!-- To Make
  Ride Wishlist
  Bikes I've Ridden
  Riding tips (?)-->
{%- assign posts = site.bike-other | sort: "order" -%}
<ul>
{%- for post in posts -%}
    <li><a href="{{ post.url | prepend: site.baseurl }}">{{post.description}}</a></li>
{%- endfor -%}
</ul>