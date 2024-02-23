---
layout: page
title: News
show_sidebar: false
hide_footer: false
permalink: /news/
---    
<div class="news">
{% if site.news != blank -%} 
<div class="table-responsive">
    <table class="table table-sm table-borderless">
    {%- assign news = site.news | reverse -%} 
    {% for item in news limit: site.news_limit %} 
    <tr>
        <th scope="row">{{ item.date | date: "%b %-d, %Y" }}</th>
        <td>
        {% if item.inline -%} 
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
        {%- else -%} 
            <a class="news-title" href=" {{ item.url | relative_url }}">{{ item.title }}</a>
        {%- endif %} 
        </td>
    </tr>
    {%- endfor %} 
    </table>
</div>
{%- else -%} 
<p>No news so far...</p>
{%- endif %} 
</div>
