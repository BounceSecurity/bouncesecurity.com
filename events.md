<table>
    {% for event in site.data.events %}
    {%if event.year != event-1.year %}
    <tr>
        <td>{{event.year}}</td>
    </tr>
    {% endif %}
    <tr>
        <td>
            {% if event.youtube %}
                <a href="{{ event.youtube }}">{{ event.title }}</a></td>
                <td><iframe width="700" height="394" src="{{ event.embed }}" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            {% else %}
                <a href="{{ event.url }}">{{ event.title }}</a>
            {% endif %}        
        </td>
    </tr>
    <tr>
        {% if event.youtube && event.url %}
            <td><a href="{{event.url}}">link to the event site</a></td>
        {% endif %}
    </tr>
    {% endfor %}
</table>