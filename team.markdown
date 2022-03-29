---
layout: page
title: Team 
permalink: /team/
---

{%- if site.data.members.size > 0-%}
    {%- for member in site.data.members -%}
        {%- include member.html member=member -%}
    {%- endfor -%}
{%- endif -%}
