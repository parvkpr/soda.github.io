---
layout: page
title: Tools
show_sidebar: false
hide_footer: false
permalink: /tools/
--- 
<div class="tools">
<h2>Tools</h2>

{% if site.tools != blank -%} 

<div class="tool-name">
    {%- for tool in site.tools %}
            <a href="{{ '' | append: tool.name | downcase | replace: '.md', ''| append: '.html' }}" class="tool-link">
                <div class="tool-m">
                    <img src="{{ tool.image | relative_url }}" alt="{{ tool.title }}" style="width:100%;">
                    <div class="container">
                        <h4><b>{{ tool.title }}</b></h4>
                    </div>
                </div>
            </a>
    {%- endfor %}
    {%- endif %}
</div>
<style>
.tool-name{
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start; /* Align items to the left */
}
.team-link {
    text-decoration: none; /* Optional: removes underline from links */
    color: inherit; /* Optional: keeps text color consistent with the rest of the design */
}
.tool-m {
    margin: 10px;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    width: 240px; /* Adjust based on your preference */
}
.tool-m:hover {
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
.container {
    padding: 2px 16px;
}
</style>