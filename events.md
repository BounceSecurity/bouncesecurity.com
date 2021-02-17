---
---

{% for event in site.data.events %}

<div class="eventsoddeven">
<a href="{{event.url}}" class="itemtxt1">{{ event.event }}</a> 
    {{ event.date }} {{event.year}}  
    {% if event.youtube %}
<span class=tab><a href="{{ event.youtube }}" class="itemtxt2">{{ event.title }}</a></span>
<iframe class="itemvid" width="262.5" height="147.75" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    {% else %}
<a href="{{ event.url }}" class="itemtxt2">{{ event.title }}</a>
    {% endif %}
</div>

{% endfor %}