---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% assign sorted_pubs = site.publications | sort: 'date' %}
{% for pub in sorted_pubs %}
  <div class="publication-item" style="margin-bottom: 1.5em;">
    <strong>{{ pub.authors }}</strong>. 
    <em>{{ pub.title }}</em> 
    {% if pub.venue %}in {{ pub.venue }}{% endif %}, {{ pub.date | date: "%Y" }}.
    <br>
    {% if pub.paperurl %}[<a href="{{ pub.paperurl }}">paper</a>]{% endif %}
    {% if pub.codeurl %}[<a href="{{ pub.codeurl }}">code</a>]{% endif %}
    {% if pub.biburl %}[<a href="{{ pub.biburl }}">bib</a>]{% endif %}
  </div>
{% endfor %}