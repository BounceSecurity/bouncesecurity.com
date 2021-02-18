---
---

<!--
{ assign sorted = site.data.events | sort: 'date' | reverse %}
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
<div class="event-youtube"><a href="{{ event.youtube }}">{{ event.title }}</a></div>
</div>
<iframe class="itemvid" width="262.5" height="147.75" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
{% else %}
<div class="event-title">{{ event.title }}</div>
{% endif %}
</div>
</div>

{% endfor %}