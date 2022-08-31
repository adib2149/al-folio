---
layout: page
permalink: /news/
title: news
description: General updates of my study, research and publications.
nav: true
order: 3
---

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% responsive_image path: assets/img/adib-conf-1.jpg class: "img-fluid rounded z-depth-1" zoomable: true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% responsive_image path: assets/img/adib-conf-2.jpg class: "img-fluid rounded z-depth-1" zoomable: true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% responsive_image path: assets/img/adib-conf-3.jpg class: "img-fluid rounded z-depth-1" zoomable: true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% responsive_image path: assets/img/adib-conf-4.png class: "img-fluid rounded z-depth-1" zoomable: true %}
    </div>
</div>

<br>

<div class="news">
  {% if site.news  %}
    <div class="table-responsive">
      <table class="table table-sm table-borderless">
      {% assign news_all = "" | split: ',' %}
      {% assign news_for_years = site.data.news  %}
      {% for news_list_in_year in news_for_years %}
        {% for each_news in news_list_in_year[1] %}
          {% assign news_all = news_all | push: each_news %}
        {% endfor %}
      {% endfor %}
      {% assign news_sorted = news_all | sort: 'date' | reverse %}

      {% for item in news_sorted %}
        <tr>
          <th scope="row" style='width: 100px;'>{{ item.date | date: "%b %-d, %Y" }}</th>
          <td>
            {% if item.new %} <mark><i>new</i></mark> {% endif %} {{ item.content | remove: '<p>' | remove: '</p>' | emojify }} {{ item.text }}
          </td>
        </tr>
      {% endfor %}
      </table>
    </div>
  {% else %}
    <p>No news so far...</p>
  {% endif %}
</div>
