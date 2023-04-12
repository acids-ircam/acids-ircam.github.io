---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
title: Articles
layout: page 
---

<div style="text-align: center; padding-bottom: 30px; width=100%;">
{%- for i in (2018..2023) reversed -%}
    <div class="article_timeline">
        <a href="#{{ i }}"> {{ i }} </a>
    </div>
{% endfor %}
</div>


{%- if site.data.members.size > 0-%}
    {%- for member in site.data.articles -%}
        {%- include article.html article=member -%}
    {%- endfor -%}
{%- endif -%}
 