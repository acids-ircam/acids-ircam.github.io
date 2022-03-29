--- 
layout: page 
title: Workshops
---



Here you will find the corresponding links of the various workshops organized by the ACIDS team.

## 2022
<ul>
  {% for ws in site.data.workshops.elements %}
    <li>
      <a href="{{ ws.url }}">{{ ws.name }} : <em> {{ ws.description }} </em> </a>
    </li>
  {% endfor %}
</ul>