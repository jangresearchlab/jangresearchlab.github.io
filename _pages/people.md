---
layout: page
title: People
permalink: /people/
nav: true
nav_order: 3
---

{% assign people = site.data.people %}

{% assign people = site.data.people %}

<div class="people-section">
  <h2>Principal Investigator</h2>
  <div class="people-grid">
    {% for p in people.pi %}
      {% include person_card.html person=p %}
    {% endfor %}
  </div>
</div>

<div class="people-section">
  <h2>Members</h2>
  <div class="people-grid">
    {% for p in people.mem %}
      {% include person_card.html person=p %}
    {% endfor %}
  </div>
</div>

<div class="people-section">
  <h2>Collaborators</h2>
  <div class="people-grid">
    {% for p in people.collabs %}
      {% include person_card.html person=p %}
    {% endfor %}
  </div>
</div>
