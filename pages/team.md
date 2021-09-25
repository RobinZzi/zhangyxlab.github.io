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

We're looking for motivated students, postdocs and research assistants to join our team. Please contact me if you are interested in our research. Click [here]({{site.url}}/{{site.baseurl}}/positions/) for more details.

##### Current members
<br>
<div class ="row">
{% for member in site.data.labmembers %}
 <div class = "small-12 medium-12 large-8 columns">
<table cellspacing="0" cellpadding="0">
 <tr> <td>
 <img src="{{site.urlimg}}{{member.image}}" alt="{{member.name}}" width="120" height="160"> 
 </td> 
<!-- </div>  <div class = "small-6 medium-3 large-3 columns"> -->
 <td> <p> <b>{{member.name}}</b> 
  <br>
 {{member.position}} <br>
 {{member.description}} 
  </p>
  </td> </tr> </table>
 </div> <!-- small-12 large-4 columns -->
{% endfor %}
</div>


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



