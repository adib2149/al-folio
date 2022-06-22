---
layout: page
permalink: /research/
title: research
description: General updates of my study, research and publications.
nav: false
---

<b>`Causal Inference`, `Computing for mHealth`, `Structural Causal Models`, `Transportability`, `Experimental Studies`, `Electronic Health Records`, `Artificial Intelligence`, `Machine Learning`, `Data Science`</b>

I was introduced to the world of `Causal Inference` <i>(by Dr. Adibuzzaman)</i> in 2018. I was immediately hooked to the fascinating works of Pearl, Elias, Rubin, Hernan, and many other researchers working relentlessly in this field. It has been a rabbit hole from there, and the more I learn, the more I find there is left to answer. I firmly believe Causal Inference is going to be one of the strongest pillars of data science in the next decades, and that is why I have decided to pursue this and make it my Ph.D. dissertation work. 

During my Ph.D., I have worked closely under the supervision of my Ph.D. Supervisor, [Dr. Sheikh Iqbal Ahamed](http://www.mscs.mu.edu/~iq/), and with direct guidance from [Dr. Mohammad Adibuzzaman](https://adibzaman.github.io/), In the past, I have worked on multiple projects involving `mobile health and computing`, `ubiquitous computing`, `crisis management`, etc. Here’s a [list](https://adib2149.github.io/research) of all the research projects I have worked on.

Other than these, I have worked on couple of other projects in mHealth, involving `Family Self-management Intervention`, `Veteran Crisis Management`, `Diabetic Retinopathy`, `Electronic Palliative Care`, and some others.

Click on the links to view: [a list of my publications](/publications), and, [a list of additional projects I have worked on](/others).

{% assign research_projects = site.research_projects %}
<div class="container">
    {% for r_project in research_projects %}
        {% include research_projects.html %}
    {% endfor %}
</div>
