---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for pub in site.publications reversed %}
__{{pub.title}}__
{{pub.date}}
{% if pub.authors %}
with {{pub.authors}}.
{% endif %}
{{pub.venue}}
{% if pub.link %} <a href="{{ pub.link }}"><i class="fas fa-fw fa-link zoom" aria-hidden="true"></i></a> {% endif %}
{% if pub.fileurl %} <a href="{{ pub.fileurl }}"><i class="fas fa-fw fa-file-pdf zoom" aria-hidden="true"></i></a> {% endif %}
{% endfor %}
