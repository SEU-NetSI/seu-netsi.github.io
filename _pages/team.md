---
title: "SEU NetSI Lab - Team"
layout: gridlay
excerpt: "SEU NetSI Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

 **We are  looking for new Master students and BSc students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**


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
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} | {{member.chinese}}</a></h4>
  <i>{{ member.info }}
  <br>Email: <{{ member.email }}>
  <br>Tel: {{ member.tel }}
  <br>Office: {{ member.office }}</i>

  <ul style="overflow: hidden">
  {% for item in member.education %}
    <li>{{ item }}</li>
  {% endfor %}
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


## Master
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} | {{member.chinese}}</a></h4>
  <i>{{ member.info }} 
  <br>Email: <{{ member.email }}></i>

  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    See More
  </button>

  <div class="collapse" id="{{ member.id }}">
    # Biography
      {% for item in member.education %}
      {{ item }}
      {% endfor %}
    # Research Interests
      {% for item in member.interest %}
      {{ item }}
      {% endfor %}
    # Correspondence 
      {% for item in member.correspondence %}
      {{ item }}
      {% endfor %}     
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
