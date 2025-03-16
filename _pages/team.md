---
title: "Team"
layout: gridlay
sitemap: false
permalink: /team/
---

### Team

**We are looking for new team members** [see vacancies](https://hbmlab-nyc.com//vacancies)!

### PI

{% for member in site.data.pi %}

<div class="jumbotron">
<div class="row">
<div class="col-sm-2">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-9 col-xs-12">
<h4>{{ member.name }}</h4>
<i>{{ member.info }}</i><br>

<ul style="overflow: hidden">
</ul>
</div>
</div>
</div>

{% endfor %}

### Current Students and Postdocs

<div class='jumbotron'>
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}

<div class="row">
{% endif %}

<div class="col-sm-2">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-4 col-xs-12">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br></i>

{% if member.website %}<a href="{{ member.website }}" target="_blank"><i class="fa fa-home fa-2x"></i></a> {% endif %}
{% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-2x"></i></a> {% endif %}
{% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-2x"></i></a> {% endif %}
{% if member.cv %} <a href="{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-2x"></i></a> {% endif %}
{% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-2x"></i></a> {% endif %}
{% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-2x"></i></a> {% endif %}

</div>
<!-- </div> -->

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}

</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}

</div>
{% endif %}
</div>

### Alumni

{% for member in site.data.alumni %}
{% if member.website %}
  <p><b>[{{ member.name }}]({{member.website}})</b>
  {% else %}
  <p><b>{{ member.name }}</b>
  {% endif %}
  Role in the lab: {{ member.role_then }} <br>
  After: {{ member.role_after }} <br></p>
 {% endfor %}



### Collaborators

- Ashesh D. Mehta, MD PhD, Feinstein Institutes
- Jose R. Herrero, PhD, Feinstein Institutes
- Nima Mesgarani, PhD, EE Columbia University
- Avniel Ghuman, PhD, UPitt
- Jack Lin, MD, UC Davis
- Bob Knight, MD, UC Berkeley
- Charles Schroeder, PhD, Nathan Kline Institute and Columbia University
- Noelle O'Connell, PhD, Nathan Kline Institute
- Sam Neymotin, PhD, Nathan Kline Institute
- Redmond O'Connell, PhD, Trinity College Dublin
- Simon Kelly, PhD, University College Dublin