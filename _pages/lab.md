---
title: "Spencer Lab Overview"
layout: gridlay
excerpt: "Spencer Lab Overview"
sitemap: false
permalink: /lab/
---

### Lab location and information
The Spencer lab is located in room 613H on the [6th floor of the Southwest Tower](https://goo.gl/maps/TwNzTrfPREB9KzSw7)
in the Wash U/Barnes-Jewish Hospital Medical Campus in St. Louis, Missouri.<br/>

We have 900 square feet of lab space with a dedicated tissue culture
room and an equipment bay with an Agilent Tapestation, Covaris
ultrafocused sonicator, three thermocyclers/thermomixers, protein and
nucleic acid electrophoresis equipment, and multiple
centrifuges. Within steps from the lab there are shared qPCR machines, imagers, plate
readers, automated protein analyzers, and Neon and Lonza
electroporation instruments. We are also located one floor below the
[Siteman flow cytometry core](https://siteman.wustl.edu/research/shared-resources-cores/flow-cytometry/),
with analyzers, sorters, and Incucyte live cell monitoring
instruments. Most computing is done on a dedicated 128 core compute cluster
with 1.5Tb of total memory. We also have access to two DRAGEN FPGA
servers for hardware-accelerated genomic analysis. 

### Current members
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
{% if member.photo %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/peoplepic/{{
  member.photo }}" class="img-responsive" width="25%" style="float:
  left" />
  {% endif %}
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

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

### Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
{% if member.photo %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/peoplepic/{{
  member.photo }}" class="img-responsive" width="25%" style="float:
  left" />
  {% endif %}
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <br/>{{ member.status }}</i>
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

