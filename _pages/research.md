---
title: "Research | SEU NetSI"
layout: textlay
excerpt: "Welcome to the SEU NetSI Group! We conducts research in the area of Internet of Things and Swarm Intelligence. Our goal is to provide theoretically sound analysis as well as build practically working systems."
sitemap: false
permalink: /research/
---

<div class="page-container">

# Research
<div class="research-list">
{% for item in site.data.research %}
<div class="panel panel-{{ item.color }}">
 <div class="panel-heading">
  <h3 class="panel-title">{{ item.topic }}</h3>
 </div>
 
 <div class="panel-body">
  <div class="row clearfix">
   <div class="col-sm-6 ">
   <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/researchpic/{{ item.image }}" class="img-thumbnail" />
   </div>

   <div class="col-sm-6 clearfix research-card-intro">
   {{ item.introduction}}
   <div>
   {% assign has_related = 0 %}

   {% for publi in site.data.publist %}
   {% if item.id == publi.category %}
   {% assign has_related = 1 %}
   {% endif %}
   {% endfor %}

   {% if has_related == 1 %}
   <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ item.id }}" aria-expanded="false" aria-controls="collapseExample">
   See More
   </button>
   {% elsif item.video != "placeholder" %}
   <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ item.id }}" aria-expanded="false" aria-controls="collapseExample">
   See More
   </button>
   {% endif %}
   </div>
   </div>
  </div>

 <div class="collapse" id="{{ item.id }}">
 {% if item.video != "placeholder" %}
 <h3>Video (YouTube)</h3>
 {% for video_item in item.video %}
 <iframe width="560" height="315" src="{{ video_item }}" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
 {% endfor %}
 {% endif %}

 {% if has_related == 1 %}
 <h3>Related Research</h3>
 {% endif %}
 <ul class="list-group">
 {% for publi in site.data.publist %}
 {% if item.id == publi.category %}
 {% assign has_related = 1 %}
 <li class="list-group-item">{{ publi.authors }}, {% if publi.link.paper != "placeholder" %} <a href="{{ publi.link.paper}}" target="_blank"><span class="label label-success pull-right pub-label">Paper</span></a>{% endif %}{% if publi.link.bibtex != "placeholder" %} <a href="{{ publi.link.bibtex}}" target="_blank"><span class="label label-default pull-right pub-label">Bibtex</span></a>{% endif %}{% if publi.link.slide != "placeholder" %} <a href="{{ publi.link.slide}}" target="_blank"><span class="label label-warning pull-right pub-label">Slides</span></a>{% endif %}{% if publi.link.video != "placeholder" %} <a href="{{ publi.link.video}}" target="_blank"><span class="label label-danger pull-right pub-label">Video</span></a>{% endif %}{% if publi.link.code != "placeholder" %} <a href="{{ publi.link.code}}" target="_blank"><span class="label label-primary pull-right pub-label">Code</span></a>{% endif %}<br />
  "{{ publi.title }}," <br />
  {{ publi.source.full }}{% if publi.source.abbr != "placeholder" %}&nbsp;<b>({{ publi.source.abbr }} {{publi.year}})</b>{% endif %}, {{ publi.source.detail }}.{% if publi.link.doi != "placeholder" %} <a href="{{ publi.link.doi}}" target="_blank"><span class="label label-info pull-right pub-label">DOI</span></a>{% endif %}</li>
 {% endif %}
 {% endfor %}
 </ul>
 </div>
</div>

</div>
{% endfor %}
</div>

</div>