---
---

<!--
{ assign sorted = site.data.events | sort: 'year' | reverse %}
{ for event in sorted %}
-->

{% for event in site.data.events %}

<div class="eventsoddeven">
<div class="event-wrapper">
<div class="event-content">
<div class="event-name">
<a href="{{event.url}}">{{ event.event }}</a>
    {{ event.date }} {{event.year}}  
</div>
    {% if event.youtube %}
<div class="event-youtube"><a href="{{ event.youtube }}">{{ event.title }}</a>
</div>
    {% else %}
        {% if event.info %}
<div class="event-title">{{ event.title }}
</div>
<div class="info"><a href="{{ event.info }}">{{ "more" }}</a>
</div>
        {% else %}
<div class="event-title">{{ event.title }}
</div>
        {% endif %}
    {% endif %}
</div>
    {% if event.youtube %}
<iframe class="itemvid" width="393.75" height="221.625" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    {% endif %}
</div>
</div>

{% endfor %}