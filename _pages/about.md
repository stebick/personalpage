---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

### About

{% for member in site.data.pi %}

<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h4>{{ member.name }}</h4>
  <h5><i>Epilepsy Attending and Assistant Professor of Neurology and Neurosurgery, Hofstra-Zucker School of Medicine, Northwell Health, NY</i></h5>
  <h5><i>Co-Director and PI at Human Brain Mapping Lab, The Feinstein Institutes for Medical Research, NY</i></h5>
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a> {% endif %}
  {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}
  {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a> {% endif %}
  {% if member.website %} <a href="{{ member.website }}" target="_blank"><i class="fa fa-image fa-3x"></i></a> {% endif %}

  <ul style="overflow: hidden">
    {% for education in member.education %}
      <li>{{ education | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>

</div>
</div>
</div>
{% endfor %}


<div class="jumbotron">
  <h4>Education</h4>
 - MD, University of Zurich, Switzerland
 - PhD, Neuroscience, University of Zurich, Switzerland  
</div>

<div class="jumbotron">
  <h4>Positions</h4>
- 2019 – now &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Faculty at the Elmezzi Graduate School, Feinstein Institutes
- 2018 – now &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Co-director [Human Brain Mapping Lab](https://hbmlab-nyc.com/), Feinstein Institutes  
- 2018 – now &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Assistant Professor, Neurology and Neurosurgery, Hofstra-Zucker School of Medicine, NY 
- 2018 – now &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Assistant Professor, Institute for Bioelectronic Medicine, Feinstein Institutes, NY 
- 2018 – now &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Epilepsy Attending, Comprehensive Epilepsy Center, Northwell Health, NY  
- 2015 – 2017	&nbsp;&nbsp;&nbsp;&nbsp; Epilepsy and Research Fellow, Stanford University, CA
- 2012 – 2015 &nbsp;&nbsp;&nbsp;&nbsp; Neurology Resident, Albert Einstein College of Medicine, Bronx, NY
- 2011 – 2012 &nbsp;&nbsp;&nbsp;&nbsp; Medicine Intern, Jacobi Medical Center, Bronx, NY
- 2009 – 2011 &nbsp;&nbsp;&nbsp;&nbsp; Postdoc, Comprehensive Epilepsy Center, North Shore - LIJ, Manhasset, NY
- 2008 – 2009	&nbsp;&nbsp;&nbsp;&nbsp; Postdoc, Program in Cognitive Neuroscience and Schizophrenia, Nathan Kline Institute, NY 
</div>

<!--
<div class="jumbotron">
  <h4>Grants</h4>
  <ul>
    {% for grant in site.data.grants %}
      <li>{{ grant.name }}</li>
    {% endfor %}
  </ul>
</div>
-->

<div class="jumbotron">
  <h4>Funding</h4>
  <img src="{{ site.url }}{{ site.baseurl }}/images/NIMH.png" width="100%" style="max-width:125px"/>
  <img src="{{ site.url }}{{ site.baseurl }}/images/NIDCD.png" width="100%" style="max-width:100px"/>
  <img src="{{ site.url }}{{ site.baseurl }}/images/NINDS-logo.png" width="100%" style="max-width:125px"/>
  <img src="{{ site.url }}{{ site.baseurl }}/images/nys-doh.png" width="100%" style="max-width:125px"/>
  <img src="{{ site.url }}{{ site.baseurl }}/images/Kavli_logo.png" width="100%" style="max-width:125px"/>
</div>

