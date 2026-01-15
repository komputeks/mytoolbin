---
title: Start Up Tools
description: Start Up Tools table
table_id: startuptools
layout: single/single-table
categories: [general-tech]
image: assets/image/png/case-details--details.png
---

{% externalJSON tabledata from url https://opensheet.elk.sh/1fVbENim7N2cdFILwVLLlet2VIT0lUyP7_mXq5sx0uio/1 %}

<div class="table table-responsive-sm">
  <table class="w-100 table-warning table-bordered table-sm" id="{{ page.table_id }}">
    {% for row in tabledata %}
      {% if forloop.first %}
      <thead>
        <tr>
          {% for pair in row %}
            <th>{{ pair[0] }}</th>
          {% endfor %}
        </tr>
      </thead>
      {% endif %}
      {% tablerow pair in row %}
        {{ pair[1] }}
      {% endtablerow %}
    {% endfor %}
  </table>
</div>
<br />

<h2>Start Up Tools</h2><br />

<div class="details-big-img  pb--50 pb-lg--75">
  <a href="https://docs.google.com/spreadsheets/d/1fVbENim7N2cdFILwVLLlet2VIT0lUyP7_mXq5sx0uio/">
    <img src="{{ page.image | relative_url }}" alt="h2_content_this_post">
  </a>
</div>