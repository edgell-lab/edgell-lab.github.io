---
layout: page
title: Publications
permalink: /publications/
---

<p class="scholar-link">Link to <a href="https://scholar.google.com/citations?user=J5Go8AMAAAAJ&hl=en" target="_blank">google scholar</a></p>

{% assign sorted = site.data.publications | sort: "year" | reverse %}
{% assign years = sorted | map: "year" | uniq %}

{% for year in years %}
<h2 class="pub-year-heading">{{ year }}</h2>
<ul class="pub-list">
  {% for pub in sorted %}
    {% if pub.year == year %}
    <li class="pub-entry">
      <div class="pub-title">{{ pub.title }}</div>
      <div class="pub-authors">{{ pub.authors }}</div>
      <div class="pub-journal">{{ pub.journal }}</div>
      {% if pub.url != "" %}
        <a class="pub-link" href="{{ pub.url }}" target="_blank">View paper &rarr;</a>
      {% endif %}
    </li>
    {% endif %}
  {% endfor %}
</ul>
{% endfor %}
