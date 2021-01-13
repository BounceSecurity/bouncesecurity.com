---
---
<style>
</style>
{% for event in site.data.events %}
    <div class=eventsoddeven>
        <div class=middle>
            <a href="{{event.url}}">{{ event.event }}</a> 
            {{ event.date }} {{event.year}}
        </div>
        <div class=middle>
            {% if event.youtube %}
                <a href="{{ event.youtube }}">{{ event.title }}</a> 
                <iframe width="262.5" height="147.75" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            {% else %}
                <a href="{{ event.url }}">{{ event.title }}</a>
            {% endif %}        
        </div>
        <div>
                 &nbsp;
        </div>
    {% endfor %}
</table>