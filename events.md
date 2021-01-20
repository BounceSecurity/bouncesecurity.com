---
---

{% for event in site.data.events %}
    {% if class.eventseven%}
<div class="eventseven">
    {% else %}
<div class="eventsodd">
<a href="{{event.url}}">{{ event.event }}</a> 
    {{ event.date }} {{event.year}}  
      
    {% if event.youtube %}
<span class=tab><a href="{{ event.youtube }}">{{ event.title }}</a></span>
<iframe width="262.5" height="147.75" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    {% else %}
<a href="{{ event.url }}">{{ event.title }}</a>
    {% endif %}
</div>

{% endfor %}