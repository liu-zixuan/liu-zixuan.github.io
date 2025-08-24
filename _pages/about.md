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
I am a postdoctoral researcher at [Centre for Quantum Information and Communication (QuIC)](http://quic.ulb.ac.be) at the Université libre de Bruxelles, working with Ognyan Oreshkov.
I received my PhD at the University of Hong Kong, supervised by [Giulio Chiribella](https://qici.weebly.com/giulio-chiribella.html). 

## research
[[arXiv]](http://arxiv.org/a/liu_z_19) [[Google scholar]](https://scholar.google.com/citations?user=cdxZIzQAAAAJ).

{% for paper in site.data.papers %}
  <p>
  <b>⚛ {{ paper[1].title }}</b>
  {% if paper[1].arxiv -%}
    <a href="https://arxiv.org/abs/{{ paper[1].arxiv }}">[arXiv:{{ paper[1].arxiv }}]</a>
  {%- endif -%}
  <br>
  {%- for author in paper[1].authors -%}
    {% if author == "Zixuan Liu" %}<u>{{ author }}</u>{% else %}{{ author }}{% endif %}
    {%- unless forloop.last -%}, {% endunless -%}
  {%- endfor -%}
  {%- if paper[1].journal -%}
    , <i><a href="{{ paper[1].doi }}">{{ paper[1].journal }}</a></i>
  {%- endif -%}
  {%- if paper[1].comment -%}
    <br>
    ({{ paper[1].comment }})
  {%- endif -%}
  </p>
{% endfor %}

## contact
Email: <{{ site.email }}>