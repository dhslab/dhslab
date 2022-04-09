---
title: "Spencer Lab Overview"
layout: gridlay
excerpt: "Spencer Lab Overview"
sitemap: false
permalink: /lab/
---

## The Spencer lab uses cutting edge approaches to understand the function of the human genome in health and disease ##

The Spencer Lab is in the Section of Stem Cell Biology in the [Division
of Oncology](https://oncology.wustl.edu/) in the
[Department of Medine](https://internalmedicine.wustl.edu/). The lab
is located on the 6th floor of the Southwest Tower in the Wash
U/Barnes-Jewish Hospital Medical Campus in St. Louis, Missouri.

Our group specializes in cancer genetics, genomics, and epigenetics
and is specifically focsed on acute myeloid leukemia (AML), a
devastating cancer that affects children and adults. Despite major
advances in the molecular understanding of this disease, current
therapies have changed little over the past 30 years. We aim to
understand 

 **We are  looking for new PhD students and Postdocs to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/jobs) **!**

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

