---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to my notes! 🌱

My name is James W. Jesso. (Check out my about page here)
Here is a repository of the notes I have taken on various videos, books, and research papers.
It is a partial export of my personal obsidian vault, meaning that some of the formatting will not be amazing. But the content is there, nonetheless.

Titles are listed as citekeys.

An important comment: these notes are taken for my own learning and understanding.
As such, there is a possibility that what I have written won't make sense to you.
Additionally, most of these were not written with the public eye in mind. There is likely to be grammar and spelling issues. 
Forgive me. 

****

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


<h2>Tags</h2>
Due to this being a partial export of my larger obsidian vault, some tags might have no links

{% assign sorted_notes = site.notes | sort: "title" %}
<ul> {% for note in sorted_notes %} {% if note.path contains "/Tags/" %} <li><a href="{{ note.url }}">{{ note.title }}</a></li> {% endif %} {% endfor %} </ul>

<h2> Graph View </h2>
<strong> Here are all the notes in this garden visualized as a graph<strong>

{% include notes_graph.html %}

.....

<h2> Also, pssst...</h2>

This site is just for $8+ patrons.
So if you are not a patron, please keep the link to this site private.

If you are not a patron, how are you here? hmm.... well, I ask you to leave in respect to the fact that this page is not meant for you. If, however, you choose to disregard this ask, at least make sure you don't share the link anywhere else! 

Thank you 🙏
