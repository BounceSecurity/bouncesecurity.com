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
        <td>
            {% if event.youtube %}
                <a href="{{ event.youtube }}">{{ event.title }}</a></td>
                <td><iframe width="262.5" height="147.75" src="{{ event.embed }}" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            {% else %}
                <class="middle"><a href="{{ event.url }}">{{ event.title }}</a></class>
            {% endif %}        
        </td>
    </tr>
    <tr> 
        <td><class="middle"> {{ event.info }} </class></td> 
    </tr>
    <tr>
            <td><class="middle"> &nbsp; <hr /> </class></td>
    </tr>
    {% endfor %}
</table>