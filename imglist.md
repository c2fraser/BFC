---
layout: page
---
<div class="container">
{% for image in site.static_files %}
    {% if image.path contains 'Photos' %}
        <img src="{{ site.baseurl }}{{ image.path }}"> {{image.name}}<br><br>
    {% endif %}
{% endfor %}
</div>
