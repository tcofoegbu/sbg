---
layout: page
title: People
permalink: /people/
---

<div class="container">
<div class="text-center">
	<div class="wow bounceInDown" data-wow-offset="0" data-wow-delay="0.3s">
	<h2>Current Group Members</h2>
	</div>    
 
{% for member in site.data.people.current_group_members %}
	{% cycle 'add rows_members' : '<div class="row">', '', '', '' %}
	<div class="col-md-3">
		<img src="{{ member.image_path | prepend: site.baseurl }}" class="img-circle" alt="">
		<h4>{{member.name}}</h4>
		<p>{{member.post}}<br/>
		<span class="glyphicon glyphicon-envelope"></span><a href="mailto:{{ member.email }}">&nbsp;{{ member.email }}</a><br/>
		<span class="glyphicon glyphicon-phone-alt"></span><a href="callto:{{ member.phone }}">&nbsp;{{ member.phone }}</a><br/>  
		<span class="glyphicon glyphicon-print"></span>&nbsp;{{ member.fax }}</p>   
	</div>
	{% cycle 'close rows_members' : '', '', '', '</div>' %}
{% endfor %}
{% cycle 'close rows_members' : '', '</div>', '</div>', '</div>' %}        
<hr/>    
<div class="wow bounceInDown" data-wow-offset="0" data-wow-delay="0.3s">
	<h2>Visitors</h2>
</div>
{% for visitor in site.data.people.group_visitors %}
	{% cycle 'add rows_visitors' : '<div class="row">', '', '', '' %}
	<div class="col-md-3">
		<img src="{{ visitor.image_path | prepend: site.baseurl }}" class="img-circle" alt="">
		<h4>{{visitor.name}}</h4>
		<p>{{visitor.info}}<br/>
		<span class="glyphicon glyphicon-envelope"></span><a href="mailto:{{ visitor.email }}">&nbsp;{{ visitor.email }}</a><br/>
		<span class="glyphicon glyphicon-phone-alt"></span><a href="callto:{{ visitor.phone }}">&nbsp;{{ visitor.phone }}</a><br/>  
		</p>   
	</div>
	{% cycle 'close rows_visitors' : '', '', '', '</div>' %}
{% endfor %}
{% cycle 'close rows_visitors' : '', '</div>', '</div>', '</div>' %}    
 <hr/>
	<div class="wow bounceInDown" data-wow-offset="0" data-wow-delay="0.3s">
		<h2>Former Group Members</h2>
	</div>
</div>
{% for f_member in site.data.people.former_group_members %}
	{% cycle 'add rows_f_member' : '<div class="row">', '', '', '' %}
	<div class="col-md-3">
		<h5><a href="{{f_member.url}}" target="_blank">{{f_member.name}}</a></h5>		              
	</div>
    {% cycle 'close rows_f_member' : '', '', '', '</div>' %}
{% endfor %}
{% cycle 'close rows_f_member' : '', '</div>', '</div>', '</div>' %}  
<br/>