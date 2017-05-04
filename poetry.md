---
layout: page
permalink: /poetry/
title: poetry
description: Published poems written by Aaron McCollough.
---

<ul class="post-list">
{% for poem in site.poetry reversed %}

{% if poem.redirect %}


        
      <li>
        <h2><a class="poem-title" href="{{ poem.redirect }}" target="_blank">{{ poem.title }}</a></h2>
        <p class="post-meta">{{ poem.date | date: '%B %-d, %Y — %H:%M' }}</p>
            </li>
      {% endif %}    
        
{% else %}

    <li>
        <h2><a class="poem-title" href="{{ poem.url | prepend: site.baseurl }}">{{ poem.title }}</a></h2>
        <p class="post-meta">{{ poem.date | date: '%B %-d, %Y — %H:%M' }}</p>
      </li>
{% endfor %}
</ul>
