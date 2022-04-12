---
title: "Spencer Lab - Publications"
layout: gridlay
excerpt: "Soencer Lab -- Publications."
sitemap: false
permalink: /publications/
---

# Publications

## Recent papers

(For a full list of publications and patents see [below](#full-list-of-publications) or go to [Google Scholar](https://scholar.google.com/citations?user=rU851-MAAAAJ&hl=en), [Pubmed](https://www.ncbi.nlm.nih.gov/myncbi/david.spencer.1/bibliography/public/))

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
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


## Patents
<em>Eric J Duncavage, David H Spencer</em><br />A streamlined
whole-genome sequencing approach for genetic profiling of cancer. (Pending) (2021)

## More publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
