{% include base_path %} {% if post.header.teaser %} {% capture teaser %}{{ post.header.teaser }}{% endcapture %} {% else %} {% assign teaser = site.teaser %} {% endif %} {% if post.id %} {% assign title = post.title | markdownify | remove: "
" | remove: "
" %} {% else %} {% assign title = post.title %} {% endif %}
{% if include.type == "grid" and teaser %}
 
{% endif %}
{% if post.link %} {{ title }} Permalink {% else %} {{ title }} {% endif %} 
{% if post.read_time %}
{% include read-time.html %}
{% endif %} {% if post.collection == 'teaching' %}
{{ post.type }}, {{ post.venue }}, {{ post.date | default: "1900-01-01" | date: "%Y" }} 
{% elsif post.collection == 'publications' %}
Published in {{ post.venue }}, {{ post.date | default: "1900-01-01" | date: "%Y" }} 
{% elsif post.date %}
{{ site.data.ui-text[site.locale].date_label | default: "Published:" }} {{ post.date | default: "1900-01-01" | date: "%B %d, %Y" }}
{% endif %} {% if post.excerpt and site.read_more != 'enabled' %}
{{ post.excerpt | markdownify }}
{% elsif post.excerpt and site.read_more == 'enabled' %}

{{ post.excerpt | markdownify | remove: '
' | remove: '
' }} Read more


{% endif %} {% if post.citation and post.paperurl %}
Recommended citation: {{ post.citation }} {{ post.paperurl }}
{% elsif post.citation %}
Recommended citation: {{ post.citation }} 
{% elsif post.paperurl %}
Download here
{% endif %} 
