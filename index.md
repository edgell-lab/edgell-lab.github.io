---
layout: default
title: Home
---

<div class="home-top">
  <div class="home-research">
    <div class="research-text">
      <h2>our research</h2>
      <p>
        I am a Professor in the
        <a href="https://www.schulich.uwo.ca/biochem/" target="_blank">Department of Biochemistry</a>
        at <a href="https://www.uwo.ca" target="_blank">Western University</a>.
        Trainees in my lab develop tools for gene editing and synthetic biology.
      </p>
      <p>
        We use evolutionary, genetic, structural and biochemical approaches to
        design, test and optimize CRISPR-based nucleases for precise and efficient
        gene editing. We apply our tools to better enable genome editing in
        eukaryotic algae, control of microbial populations, and treatment of
        human disease.
      </p>
      <p><a href="{{ '/research/' | relative_url }}">Learn more about our research &rarr;</a></p>

      <div class="home-news">
        <h2>news</h2>
        <ul class="news-list">
          {% for item in site.data.news %}
          <li>
            {% if item.url %}
              {{ item.text | replace: item.link, '' | strip }}
              <a href="{{ item.url }}" target="_blank">{{ item.link }}</a>
            {% else %}
              {{ item.text }}
            {% endif %}
          </li>
          {% endfor %}
        </ul>
      </div>
    </div>

    <div class="research-image">
      <img src="{{ '/assets/images/performative_students.jpeg' | relative_url }}" alt="Edgell Lab Students" />
      <img src="{{ '/assets/images/graphical_abstract.png' | relative_url }}" alt="Graphical Abstract" />
    </div>
  </div>
</div>

<div class="latest-pubs">
  <h2>latest publications</h2>
  {% assign recent = site.data.publications %}
  <div class="pub-cards">
    {% for pub in recent limit:3 %}
    <div class="pub-card">
      {% if pub.cover_image and pub.cover_image != "" %}
        <img src="{{ '/assets/images/' | append: pub.cover_image | relative_url }}" alt="{{ pub.title }}">
      {% endif %}
      <div class="pub-card-body">
        <h3>
          {% if pub.url != "" %}
            <a href="{{ pub.url }}" target="_blank">{{ pub.title }}</a>
          {% else %}
            {{ pub.title }}
          {% endif %}
        </h3>
        <p>{{ pub.authors }}</p>
        <p><em>{{ pub.journal }}</em> ({{ pub.year }})</p>
      </div>
    </div>
    {% endfor %}
  </div>
  <p style="margin-top:1.5rem"><a href="{{ '/publications/' | relative_url }}">See all publications &rarr;</a></p>
</div>
