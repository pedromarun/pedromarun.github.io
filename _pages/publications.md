---
layout: archive
title: "Research"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<h2> In preparation </h2>

{% for pub in site.talks reversed %}
{% if pub.authors %}
__{{pub.title}}__\
with {{pub.authors}}.
{% endif %}

{% if pub.self %}
__{{pub.title}}__
{% endif %}
{% endfor %}

<h2> Preprints </h2>

{% for pub in site.portfolio reversed %}
{% if pub.authors %}
__{{pub.title}}__\
with {{pub.authors}}.\
{{pub.venue}}. ({{pub.date | date: "%Y" }}) {% if pub.link %} <a href="{{ pub.link }}"><i class="fas fa-fw fa-link zoom" aria-hidden="true"></i></a> {% endif %} {% if pub.fileurl %} <a href="{{ pub.fileurl }}"><i class="fas fa-fw fa-file-pdf zoom" aria-hidden="true"></i></a> {% endif %}
{% endif %}

{% if pub.self %}
__{{pub.title}}__\
{{pub.venue}}. ({{pub.date | date: "%Y" }}) {% if pub.link %} <a href="{{ pub.link }}"><i class="fas fa-fw fa-link zoom" aria-hidden="true"></i></a> {% endif %} {% if pub.fileurl %} <a href="{{ pub.fileurl }}"><i class="fas fa-fw fa-file-pdf zoom" aria-hidden="true"></i></a> {% endif %}
{% endif %}
{% endfor %}

<h2> Published papers </h2>

{% for pub in site.publications reversed %}
{% if pub.authors %}
__{{pub.title}}__\
with {{pub.authors}}.\
{{pub.venue}}. ({{pub.date | date: "%Y" }}) {% if pub.link %} <a href="{{ pub.link }}"><i class="fas fa-fw fa-link zoom" aria-hidden="true"></i></a> {% endif %} {% if pub.fileurl %} <a href="{{ pub.fileurl }}"><i class="fas fa-fw fa-file-pdf zoom" aria-hidden="true"></i></a> {% endif %}
{% endif %}

{% if pub.self %}
__{{pub.title}}__\
{{pub.venue}}. ({{pub.date | date: "%Y" }}) {% if pub.link %} <a href="{{ pub.link }}"><i class="fas fa-fw fa-link zoom" aria-hidden="true"></i></a> {% endif %} {% if pub.fileurl %} <a href="{{ pub.fileurl }}"><i class="fas fa-fw fa-file-pdf zoom" aria-hidden="true"></i></a> {% endif %}
{% endif %}
{% endfor %}
