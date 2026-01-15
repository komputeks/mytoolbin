---
title: My Bookmarks
description: This is the description of my bookmarks
table_id: my_bookmarks
layout: single/single-table
categories: [general-tech]
image: assets/image/png/case-details--details.png
---
 
{% externalJSON tabledata from url https://opensheet.elk.sh/1TZYN2wH9EP9pCxp7fGsku9QUnODaQ06m28GNZqn2dfI/1 %}

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

<h2>My Bookmarks</h2><br />

<div class="details-big-img  pb--50 pb-lg--75">
  <a href="https://docs.google.com/spreadsheets/d/1TZYN2wH9EP9pCxp7fGsku9QUnODaQ06m28GNZqn2dfI/">
    <img src="{{ page.image | relative_url }}" alt="h2_content_this_post">
  </a>
</div>