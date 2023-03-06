---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on &lt;u&gt;&lt;a href="{{author.googlescholar}}"&gt;my Google Scholar profile&lt;/a&gt;.&lt;/u&gt;
{% endif %}

{% include base_path %}

{% for pub in site.publications reversed %}
__{{pub.title}}__\
with {{pub.authors}}.\
{{pub.venue}}
{% if pub.link %} &lt;a href="{{ pub.link }}"&gt;&lt;i class="fas fa-fw fa-link zoom" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt; {% endif %}
{% if pub.fileurl %} &lt;a href="{{ pub.fileurl }}"&gt;&lt;i class="fas fa-fw fa-file-pdf zoom" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt; {% endif %}
{% endfor %}