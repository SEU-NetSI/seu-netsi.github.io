---
title: "Gallery | SEU NetSI"
layout: piclay
excerpt: "Welcome to the SEU NetSI Group! We conducts research in the area of Internet of Things and Swarm Intelligence. Our goal is to provide theoretically sound analysis as well as build practically working systems."
permalink: /gallery/
---

<div class="page-container">

# Gallery
Jump to [Our Group](#our-group), [Southeast University](#southeast-university). 


## Our Group
Record Life, Record Us.<br>
{% assign number_printed = 0 %}
{% assign even_odd = 0 %}
{% for pic in site.data.pics.ourgroup %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix gallery-pic text-warning">
<img src="{{ site.url }}{{ site.baseurl }}/images/gallery/{{ pic.image }}" class="img-responsive img-rounded" width="100%" style="float: left" />
{{ pic.intro }} <br><span class="label label-default">{{ pic.date }}</span>
</div>

{% assign number_printed = number_printed | plus: 1 %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
</div>
{% endif %}

{% endfor %}


## Southeast University
The first 3 pictures in the first row are taken in Sipailou Campus (Since 1902), <br> the other pictures in the next rows are taken in Jiulonghu Campus (Since 2006).<br>

{% assign number_printed = 0 %}
{% assign even_odd = 0 %}
{% for pic in site.data.pics.seuview %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-4 clearfix gallery-pic text-success">
<img src="{{ site.url }}{{ site.baseurl }}/images/gallery/{{ pic.image }}" class="img-responsive img-rounded"  width="100%" style="float: left" />
{{ pic.intro }} <br>
</div>

{% assign number_printed = number_printed | plus: 1 %}
{% assign even_odd = number_printed | modulo: 3 %}
{% if even_odd == 0 %}
</div>
{% endif %}

{% endfor %}

</div>