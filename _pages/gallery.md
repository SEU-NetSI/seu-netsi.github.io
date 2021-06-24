---
title: "Gallery | SEU NetSI"
layout: piclay
excerpt: "Welcome to the SEU NetSI Group! We conducts research in the area of Internet of Things and Swarm Intelligence. Our goal is to provide theoretically sound analysis as well as build practically working systems."
permalink: /gallery/
---

<div class="page-container">

# Gallery
Record Life, Record Us.<br>

## Our Group
(Right-click *'view image'* to see a larger image)
{% assign number_printed = 0 %}
{% for pic in site.data.pics.ourgroup %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix gallery-pic text-primary">
<img src="{{ site.url }}{{ site.baseurl }}/images/gallery/{{ pic.image }}" class="img-responsive img-rounded" width="100%" style="float: left" />
{{ pic.intro }} <br><span class="label label-default">{{ pic.date }}</span>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd > 2 %}
</div>
{% endif %}


{% endfor %}

{% assign even_odd = number_printed | modulo: 4 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% if even_odd == 3 %}
</div>
{% endif %}

## Southeast University
(Right-click *'view image'* to see a larger image)
{% assign number_printed = 0 %}
{% for pic in site.data.pics.seuview %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/gallery/{{ pic.image }}" class="img-responsive img-rounded"  width="100%" style="float: left" />
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd > 2 %}
</div>
{% endif %}


{% endfor %}

{% assign even_odd = number_printed | modulo: 4 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% if even_odd == 3 %}
</div>
{% endif %}

</div>