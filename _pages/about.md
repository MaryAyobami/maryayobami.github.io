---
layout: about
title: about
permalink: /
subtitle: Ph.D. Student in Computer Science at <a href='https://www.cs.utah.edu/'>University of Utah</a>

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>MEB Room 3490A</p>
    <p>50 South Central Campus Drive</p>
    <p>University of Utah</p>
    <p>Salt Lake City, UT 84112</p>

<!-- selected_papers: true # includes a list of papers marked as "selected={true}" -->
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 3 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am Mary Ogunmola, a Computer Science Ph.D. student at the University of Utah, where I am advised by [Professor Robert Ricci](https://www.cs.utah.edu/~ricci/) in the [Flux Research Group](https://www.flux.utah.edu/). I am interested in security, verifiable trust, and performance. Broadly, my research explores how cloud workloads can maintain strong security and trust guarantees, as well as how systems experiments can produce more reliable, representative, and reproducible results. You can read more about my current research areas [here](/research/).

Before my doctoral studies, I worked for a year building web applications and automating secure deployment pipelines. I also have experience in technical writing, and I am passionate about making technical knowledge more accessible.

<p>{{ site.contact_note }} <a href="mailto:{{ site.data.socials.email | encode_email }}">send me an email</a>.</p>

<h2 id="service">service</h2>

{% include service.liquid %}
