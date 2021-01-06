---
---

<table>
    {% for event in site.data.events %}
        <td>
            {% if event.youtube %}
                <a href="{{ event.youtube }}">{{ event.title }}</a></td>
                <td><iframe width="700" height="394" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            {% else %}
                <a href="{{ event.url }}">{{ event.title }}</a>
            {% endif %}        
        </td>
    </tr>
    <tr>
        {% if event.youtube && event.url %}
            <td></td>
            <td><a href="{{event.url}}">Click here for more</a></td>
            <td></td>
        {% endif %}
    </tr>
    <tr> </tr>
    {% endfor %}
</table>