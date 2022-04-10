---
title: "Spencer Lab Overview"
layout: gridlay
excerpt: "Spencer Lab Overview"
sitemap: false
permalink: /lab/
---

###The Spencer lab
![cap](/images/logopic/wusm.png){:width="150px"
style="float: left; border-radius:0%"} The Spencer Lab is in the Section of Stem Cell Biology in the [Division
of Oncology](https://oncology.wustl.edu/) in the
[Department of Medine](https://internalmedicine.wustl.edu/) at
[Washington University School of Medicine in St. Louis](https://medicine.wustl.edu/). The lab is located on the
[6th floor of the Southwest Tower](https://goo.gl/maps/TwNzTrfPREB9KzSw7)
in the Wash U/Barnes-Jewish Hospital Medical Campus in St. Louis, Missouri. 

![Human Genome](/images/respic/humangenome.jpg){:width="150px"
  id="" style="float:right; border-radius:0%;background-color:white"} **Research in the Spencer lab is a combination of experimental and
  computational science with a common theme of genomics.** We
  have specific expertise in DNA methylation, 3D genome architecture, and
  HOX gene expression and regulation, although we are broadly interested in
  epigenetics and gene
  regulation. To study these topics we use a range of experimental systems and techniques, including:
  * Whole-exome sequencing, whole-genome sequencing, error-corrected
    amplicon sequencing
  * Long read sequencing using Oxford Nanopore and PacBio Hifi platforms
  * ChIP-seq, RNA-seq, ATAC-seq
  * whole-genome bisulfite sequencing
  * CUT&Run, CUT&Tag
  * in situ HiC, capture-C, HiChIP, PLAC-seq
  * CRISPR/Cas9 genome editing, CRISPRi epigenetic editing
  * CRE-seq massively parallel reporter assays
  * Single cell technologies
  * Human cell lines
  * Human pluripotent stem cells, including NIH-approved embryonic
  stem cells and induced pluripotent stem (iPS) cells.
  * Primary human AML samples
  * Mouse models

We have direct access to high-throughput sequencers and cutting edge
genomic methods at the McDonnell Genome Institute via David's role as
Medical Director of the CLIA sequencing lab. We perform our own data analysis on a dedicate compute cluster using
analysis pipelines that we developed and implemented for our
research. 

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

