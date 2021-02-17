---
---

<>
{% for event in site.data.events %}

<div class="eventsoddeven">
<div class="itemtxt"><a href="{{event.url}}">{{ event.event }}</a>
    {{ event.date }} {{event.year}}  
    {% if event.youtube %}
<span class=tab><a href="{{ event.youtube }}">{{ event.title }}</a></span></div>
<iframe class="itemvid" width="262.5" height="147.75" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    {% else %}
<a href="{{ event.url }}">{{ event.title }}</a></div>
    {% endif %}
</div>

{% endfor %}
<div> //display flex
    <div>
        <p>
        </p>
        <p>
        </p>
    </div>
    <iframe>
</div>