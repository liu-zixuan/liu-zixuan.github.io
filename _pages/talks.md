---
layout: default
permalink: /talks/
title: talks
nav: true
---


<table>

<tr>
    <th>conference</th>
    <th>title</th> 
    <th>attachment</th>
</tr>

    {% for talk in site.data.talks %}
<tr>
    <td>{{ talk[1].conference }}</td>
    <td>{{ talk[1].title }}</td>
    {% if talk[1].attachment %}
    <td><a href="{{ talk[1].pdf | append: '.pdf' | prepend: 'assets/pdf/' | relative_url }}">{{ talk[1].attachment }}</a></td>
    {% else %}
    <td></td>
    {% endif %}
</tr>
    {% endfor %}
  
</table>