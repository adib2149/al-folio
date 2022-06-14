---
layout: page
permalink: /research/
title: research
description: General updates of my study, research and publications.
nav: false
---

<b>`Causal Inference`, `Computing for mHealth`, `Structural Causal Models`, `Transportability`, `Experimental Studies`, `Electronic Health Records`, `Artificial Intelligence`, `Machine Learning`, `Data Science`</b>

Broad level overview of projects 

Other than these, I have worked on couple of other projects in mHealth, involving `Family Self-management Intervention`, `Veteran Crisis Management`, `Diabetic Retinopathy`, `Electronic Palliative Care`, and some others.

Click on the links to view: [a list of my publications](/publications), and, [a list of additional projects I have worked on](/others).

{% assign research_projects = site.research_projects %}
<div class="container">
    {% for r_project in research_projects %}
        {% include research_projects.html %}
    {% endfor %}
</div>
