---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to my notes! 🌱

My name is James W. Jesso. (Check out my about page here)
Here is a repository of the notes I have taken on various videos, books, and research papers.

<h4> Some important points prior to exploring</h4>
<ul>
<li>Titles are listed as citekeys.
<li>Subheading describe the general note I am taking.
<li>Content under each subheading is my own, unless it is in blockquote style, which means it is from the author of the book/paper/video I am taking notes on. 
<li>This is a partial export of my personal obsidian vault, meaning that some of the formatting will not be amazing, some links will try and open applications (e.g. my reference manager), and some linked notes will not go anywhere.
<li>These notes are taken for my own learning and understanding. As such, there is a possibility that what I have written won't make sense to you.
<li>Most of these were not written with the public eye in mind. There is likely to be grammar and spelling issues. 
</ul>





<h2>Recently updated notes</h2>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>


<h2>All Notes </h2>

{% assign sorted_notes = site.notes | sort: "title" %} <ul> {% for note in sorted_notes %} {% if note.path contains "/Research Notes/" %} <li><a href="{{ note.url }}">{{ note.title }}</a></li> {% endif %} {% endfor %} </ul>

<h2> TAGS</h2>
Due to this being a partial export of my larger obsidian vault, some tags might have no links

{% assign sorted_notes = site.notes | sort: "title" %}
<ul> {% for note in sorted_notes %} {% if note.path contains "/Tags/" %} <li><a href="{{ note.url }}">{{ note.title }}</a></li> {% endif %} {% endfor %} </ul>

<h2> Graph View </h2>
Here are all the notes in this garden visualized as a graph

{% include notes_graph.html %}

