---
title: Cecile All Songs
description: no desc
table_id: cecile_all_songs
layout: single/single-table
categories: [artist-collection]
---

{% externalJSON tabledata from url https://opensheet.elk.sh/10PEtcdOPfGEQROw7q4gYLXkTECaKymuYzJv76bP6KNw/1 %}
 
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

<h2>All Cecile Songs</h2>


<div class="details-big-img  pb--50 pb-lg--75">
  <img src="https://wpsstrapicms.cache.wpscdn.com/56_2832fb1ed8.png" alt="h2_content_this_post">
</div>