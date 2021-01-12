---
---
{% for event in site.data.events %}
    <table border = "1px">
        <tr>
            <td>{{ event.event }}</td>
            <td>{{ event.date }} {{event.year}}</td>
        </tr>
        <tr>
            <td>
                {% if event.youtube %}
                    <a href="{{ event.youtube }}">{{ event.title }}</a></td>
                    <td><iframe width="525" height="295.5" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                {% else %}
                    <center><a href="{{ event.url }}">{{ event.title }}</a></center>
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
        <tr> <td> </td> </tr>
    </table>
    {{events.info}}
{% endfor %}