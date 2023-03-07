---
layout: archive
title: "Talks"
permalink: /talks/
author_profile: true
---

{% include base_path %}

{% for talk in site.talks reversed %}
__{{talk.title}}__\
{{talk.date | date: "%-d %B %Y" }}\
{{talk.venue}}\
{% if talk.fileurl %}
[Slides]{talk.fileurl}
{% endif %}
{% endfor %}