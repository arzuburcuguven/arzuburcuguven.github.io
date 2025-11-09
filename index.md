---
# layout: splash
permalink: /
layout: single
author_profile: true
#title: Home
---

## About

I am a PhD student in Data Science at IT University of Copenhagen.
I work in the [NLPnorth](https://nlpnorth.github.io/) research group, under the supervision of [Rob van der Goot](https://robvanderg.github.io/) and [Anna Rogers](https://annargrs.github.io/).

My research focuses on how language models learn and use language, specifically I am interested in whether language models develop hierarchical biases toward syntactic structure, how we can distinguish statistical learning from structural 
knowledge, and how training data composition affects model performance. Broader themes in my work are generalization, and multilingual linguistic evaluation.

## Publications

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
