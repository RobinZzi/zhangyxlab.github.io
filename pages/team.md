---
layout: page-fullwidth
title: "Team"
header:
  image: "ZhangLab_logo.png"
  background-color: "#FFFFFF"

meta_title: "Lab members"
subheadline: # "Awesome team"
permalink: "/team/"
---
##### Current members
<br>
<div class ="row">
{% for member in site.data.labmembers %}
 <div class = "small-12 medium-6 large-3 columns">
 {% if member.image %}  <img src="{{site.urlimg}}{{member.image}}"> {% endif %}
 <p> <b>{{member.name}}</b>
  <br>
 {{member.position}} <br>
  </p>
 </div> <!-- small-12 large-4 columns -->
{% endfor %}
</div>

We're actively recruiting students, postdocs and research assistants. Please contact me if you are interested in our research. 

{%comment %}

##### Alumni

<table>
 <tr><th> Name </th> <th>Prev. Pos</th>><th> Year</th> <th> Curr. Pos </th> </tr>
{% for member in site.data.alumni %}
 <tr>
 <td> <b>{{member.name}} </b>
 {% if member.url %} <a href="{{member.url}}"> &lt;website&gt;</a> {% endif %} </td>
 <td> {{member.prev_position}} </td>
 <td>{{member.year}} </td>
 <td>{{member.curr_position}} </td>
 </tr>
{% endfor %}
</table>

(Please contact website <a href="mailto:zhangyanxiao@westlake.edu.cn">admin</a> to correct any mistakes or missing information.)
{% endcomment %}



