---
layout: page
permalink: /news-old/
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
      {% assign news = site.news | reverse %}
      {% assign last_item_year = "now" | date: "%Y" %}
      {% for item in news %}
        <tr>
          <th scope="row" style='width: 100px;'>{{ item.date | date: "%b %-d, %Y" }}</th>
          <td>
            {% if item.inline %}
            {% if item.new %} <mark><i>new</i></mark> {% endif %} {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
            {% else %}
              <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
            {% endif %}
          </td>
        </tr>
      {% endfor %}
      </table>
    </div>
  {% else %}
    <p>No news so far...</p>
  {% endif %}
</div>
