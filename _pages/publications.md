---
title: "SEU NetSI - Publications"
layout: gridlay
excerpt: "Publications."
sitemap: false
permalink: /publications/
---

# Publications
## Group Highlights

For a full list of publications and patents see [below](#full-list-of-publications) or go to [Google Scholar](https://scholar.google.com/citations?user=7N_fRVwAAAAJ).

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Full List of Publications

{% for publi in site.data.publist %}
  <div class="well-sm">
  {{ publi.title }} <br />
  {{ publi.authors }} <br />
  {{ publi.source.full }}&nbsp;<b>({{ publi.source.abbr }} {{publi.year}})</b>
  {% if publi.link.paper != "placeholder" %} <a href="{{ publi.link.paper}}" target="_blank"><span class="label label-success pull-right pub-label">Paper</span></a>{% endif %}
  {% if publi.link.slide != "placeholder" %} <a href="{{ publi.link.slide}}" target="_blank"><span class="label label-warning pull-right pub-label">Slides</span></a>{% endif %}
  {% if publi.link.code != "placeholder" %} <a href="{{ publi.link.code}}" target="_blank"><span class="label label-primary pull-right pub-label">Code</span></a>{% endif %}
  </div>
{% endfor %}
