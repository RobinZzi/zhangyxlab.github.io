---
layout: page-fullwidth
title: "Team"
meta_title: "Lab members"
subheadline: # "Wufoo-powered contact forms"
#teaser: "Get in touch with me? Use the contact form."
permalink: "/team/"
---
##### Principle Investigator
<br>
 <img src="{{site.urlimg}}team-bingren.jpg">
<b> <a href="http://www.ludwigcancerresearch.org/location/san-diego-branch/bing-ren-lab"> Bing Ren, PhD. </a> </b>
<hr>
##### Current members
<br>
<table>
{% for member in site.data.labmembers %}
 <tr>
 <td> <b>{{member.name}} </b>
 {% if member.url %} <a href="{{member.url}}"> &lt;website&gt;</a> {% endif %} </td>
 <td>{{member.position}} </td>
 <td>{{member.email}} </td>
 </tr>
{% endfor %}
</table>
<hr>
##### Alumni (incomplete)
