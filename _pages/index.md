---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to my notes! 🌱

Here is a repository of the notes I have taken on various videos, books, and research papers.

This is just for $8+ patrons.
So if you are not a patron, please keep the link to this site private.

If you are not a patron, how are you here? hmm.... well, I ask you to leave in respect to the fact that this page is not meant for you. If, however, you choose to disregard this ask, at least make sure you don't share the link anywhere else! Thank you 🙏


<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 10 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<p>
<strong> Here are all the notes in this garden, along with their links, visualized as a graph<strong>
</p>

{% include notes_graph.html %}


<style>
  .wrapper {
    max-width: 46em;
  }
</style>
