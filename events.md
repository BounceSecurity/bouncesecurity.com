---
---
<style>

    </style>
<table class="eventtable">
    {% for event in site.data.events %}
    <tr>
        <td><a href="{{event.url}}">{{ event.event }}</a></td>
        <td>{{ event.date }} {{event.year}}</td>
    </tr>
    <tr>
            {% if event.youtube %}
        <td>
                <a href="{{ event.youtube }}">{{ event.title }}</a></td>
                <td><iframe width="262.5" height="147.75" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                </td>
            {% else %}
            <td colspan="2"><a href="{{ event.url }}">{{ event.title }}</a>
        </td>
            {% endif %}        
    </tr>
    <tr> 
        <td colspan="2">{{ event.info }}</td>
    </tr>
    <tr>
            <td colspan="2"> &nbsp; <hr /></td>
    </tr>
    {% endfor %}
</table>