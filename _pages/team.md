---
title: "SEU NetSI - Team"
layout: gridlay
excerpt: "Team"
sitemap: false
permalink: /team/
---

# Group Members

Jump to [staff](#staff), [master](#master), [alumni](#alumni).

## Staff
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-9 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} {% if member.chinese != "placeholder" %} | {{member.chinese}}{% endif %}</a></h4>
  <i>{{ member.info }}
  <br>Email: <{{ member.email }}>
  <br>Tel: {{ member.tel }}
  <br>Office: {{ member.office }}</i>

  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
  See More
  </button>
  <br><br>
  
  <div class="collapse" id="{{ member.id }}">
  <h3>Biography</h3>
  {{ member.biography }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## Master
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} {% if member.chinese != "placeholder" %} | {{member.chinese}}{% endif %}</a></h4>
  <i>{{ member.info }} 
  <br>Email: <{{ member.email }}></i>

  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    See More
  </button>

  <div class="collapse" id="{{ member.id }}">

  <h3>Biography</h3>
  <div>
  <ul>
  {% for item in member.education %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Interests</h3>
  <div>
  <ul>
  {% for item in member.interest %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Correspondence</h3>
  <div>
  <ul>
  {% for item in member.correspondence %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} | {{member.chinese}}</a></h4>
  <i>{{ member.info }}
  <br>Email: <{{ member.email }}></i>
  <ul style="overflow: hidden">
  
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Visitors, Bachelor Students
<div class="row">

<div class="col-sm-6 clearfix">
<h4>Visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-6 clearfix">
<h4>Bachelor Students</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div>
