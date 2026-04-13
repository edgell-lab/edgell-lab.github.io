---
layout: page
title: People
permalink: /people/
---

<h2 class="people-section-heading">Principal Investigator</h2>
<div class="people-grid">
  {% for person in site.data.people.pi %}
  <div class="person-card">
    {% if person.photo != "" %}
      <img src="{{ '/assets/images/' | append: person.photo | relative_url }}" alt="{{ person.name }}">
    {% else %}
      <div class="person-photo-placeholder">&#128100;</div>
    {% endif %}
    <div class="person-name">{{ person.name }}</div>
    <div class="person-role">{{ person.role }}</div>
    {% if person.bio %}<p style="font-size:0.85rem;margin-top:0.5rem">{{ person.bio }}</p>{% endif %}
    <div class="person-links">
      {% if person.email %}<a href="mailto:{{ person.email }}">Email</a>{% endif %}
      {% if person.twitter %}<a href="https://twitter.com/{{ person.twitter }}" target="_blank">Twitter</a>{% endif %}
    </div>
  </div>
  {% endfor %}
</div>

{% if site.data.people.postdocs.size > 0 %}
<h2 class="people-section-heading">Postdoctoral Fellows</h2>
<div class="people-grid">
  {% for person in site.data.people.postdocs %}
  <div class="person-card">
    {% if person.photo != "" %}
      <img src="{{ '/assets/images/' | append: person.photo | relative_url }}" alt="{{ person.name }}">
    {% else %}
      <div class="person-photo-placeholder">&#128100;</div>
    {% endif %}
    <div class="person-name">{{ person.name }}</div>
    <div class="person-role">{{ person.role }}</div>
  </div>
  {% endfor %}
</div>
{% endif %}

<h2 class="people-section-heading">Current Graduate Trainees</h2>
<ul class="alumni-list">
  {% for person in site.data.people.grad_students %}
  <li>
    <span class="alumni-name">{{ person.name }}</span> &mdash;
    <span class="alumni-role">{{ person.role }}</span>
  </li>
  {% endfor %}
</ul>

{% if site.data.people.undergrads.size > 0 %}
<h2 class="people-section-heading">Undergraduate Researchers</h2>
<div class="people-grid">
  {% for person in site.data.people.undergrads %}
  <div class="person-card">
    {% if person.photo != "" %}
      <img src="{{ '/assets/images/' | append: person.photo | relative_url }}" alt="{{ person.name }}">
    {% else %}
      <div class="person-photo-placeholder">&#128100;</div>
    {% endif %}
    <div class="person-name">{{ person.name }}</div>
    <div class="person-role">{{ person.role }}</div>
  </div>
  {% endfor %}
</div>
{% endif %}

<h2 class="people-section-heading">Alumni</h2>
<ul class="alumni-list">
  {% for person in site.data.people.alumni %}
  <li>
    <span class="alumni-name">{{ person.name }}</span> &mdash;
    <span class="alumni-role">{{ person.role }}</span>
  </li>
  {% endfor %}
</ul>
