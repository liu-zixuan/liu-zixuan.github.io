---
layout: about
title: about
permalink: /
subtitle: 

# profile:
#   align: right
#   image: prof_pic.jpg
#   image_circular: false # crops the image to make it circular
#   address: >
#     <p>555 your office number</p>
#     <p>123 your address street</p>
#     <p>Your City, State 12345</p>

# news: true  # includes a list of news items
# selected_papers: true # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---

## about me
I am a fourth year PhD student of [Quantum Information and Computation Initiative](https://qici.weebly.com) led by [Prof. Giulio Chiribella](https://qici.weebly.com/giulio-chiribella.html) at The University of Hong Kong. My research field is quantum information and quantum foundations. I received my BEng degree in computer science at Zhejing University.

## research
<ul>
{% for paper in site.data.papers %}
  <li>
    {% if paper.url %}
      <a href="{{ paper.url }}">
        <b>{{ paper.title }}</b>
      </a>
    {% else %}
      <b>{{ paper.title }}</b>
    {% endif %}
    --
    {% for author in paper.authors %}
      {% if forloop.last %}
        {{ author }}
      {% else %}
        {{ author }},
      {% endif %}
    {% endfor %}
    <br>
    <i>{{ paper.journal }}</i>
    {% if paper.comment %}
      ({{ paper.comment }})
    {% endif %}
  </li>
{% endfor %}
</ul>

## contact
Email: <{{ site.email }}>