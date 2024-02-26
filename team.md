---
layout: page
title: Our Team
show_sidebar: false
hide_footer: false
permalink: /team/
hero_height: is-large
hero_image: /assets/img/team1.jpg
---

<div class="team">

{% if site.team != blank -%} 

<!-- Faculty Section -->
<h3>Faculty</h3>
<div class="team-members">
    {%- for member in site.team %}
        {%- if member.category == 'faculty' %}
            <a href="{{ '' | append: member.name | downcase | replace: '.md', ''| append: '.html' }}" class="team-member-link">
                <div class="team-member">
                    <img src="{{ member.image | relative_url }}" alt="{{ member.title }}" style="width:100%;">
                    <div class="container">
                        <h4><b>{{ member.title }}</b></h4>
                        {{ member.job_title }}
                    </div>
                </div>
            </a>
        {%- endif %}
    {%- endfor %}
</div>

<!-- Postdoc Section -->
<h3>Postdocs</h3>
<div class="team-members">
    {%- for member in site.team %}
        {%- if member.category == 'postdoc' %}
            <a href="{{ '' | append: member.name | downcase | replace: '.md', ''| append: '.html' }}" class="team-member-link">
                <div class="team-member">
                    <img src="{{ member.image | relative_url }}" alt="{{ member.title }}" style="width:100%;">
                    <div class="container">
                        <h4><b>{{ member.title }}</b></h4>
                        {{ member.job_title }}
                    </div>
                </div>
            </a>
        {%- endif %}
    {%- endfor %}
</div>

<!-- PhD Student Section -->
<h3>PhD Students</h3>
<div class="team-members">
    {%- for member in site.team %}
        {%- if member.category == 'phd_student' %}
            <a href="{{ '' | append: member.name | downcase | replace: '.md', ''| append: '.html' }}" class="team-member-link">
                <div class="team-member">
                    <img src="{{ member.image | relative_url }}" alt="{{ member.title }}" style="width:100%;">
                    <div class="container">
                        <h4><b>{{ member.title }}</b></h4>
                        {{ member.job_title }}
                    </div>
                </div>
            </a>
        {%- endif %}
    {%- endfor %}
</div>

<!-- Alumni -->
<h3>Alumni</h3>
<div class="team-members">
    {%- for member in site.team %}
        {%- if member.category == 'alumni' %}
            <a href="{{ '' | append: member.name | downcase | replace: '.md', ''| append: '.html' }}" class="team-member-link">
                <div class="team-member">
                    <img src="{{ member.image | relative_url }}" alt="{{ member.title }}" style="width:100%;">
                    <div class="container">
                        <h4><b>{{ member.title }}</b></h4>
                        {{ member.job_title }}
                    </div>
                </div>
            </a>
        {%- endif %}
    {%- endfor %}
</div>
{%- else -%} 
<p>No team members listed so far...</p>
{%- endif %} 
</div>

<style>
.team-members {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start; /* Align items to the left */
}
.team-member-link {
    text-decoration: none; /* Optional: removes underline from links */
    color: inherit; /* Optional: keeps text color consistent with the rest of the design */
}
.team-member {
    margin: 10px;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    width: 240px; /* Adjust based on your preference */
}
.team-member:hover {
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
.container {
    padding: 2px 16px;
}
</style>
