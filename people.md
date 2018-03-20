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
 
{%- for member in site.data.people.current_group_members %}
	{%- cycle 'add rows_members' : '<div class="row">', '', '', '' %}
	<div class="col-md-3">
		{%- if member.image_path != null and member.image_path != "" %}
			<img src="{{ member.image_path | prepend: site.baseurl }}" class="img-circle" alt="">	
		{%- else %}			
			<img src="{{ "/assets/images/people/blank_man.png" | prepend: site.baseurl }}" class="img-circle" alt="">	
		{%- endif %}  
		{%- if member.url != null and member.url != "" %}
		<h4><a href="{{member.url}}" target="_blank">{{member.name}}</a></h4>		
		{%- else %}	
		<h4>{{member.name}}</h4>		
		{%- endif %} 
		{%- if member.post != null and member.post != "" %}
			<p>{{member.post}}<br/>		
		{%- endif %}  
		{%- if member.email != null and member.email != "" %}
			<span class="glyphicon glyphicon-envelope"></span><a href="mailto:{{ member.email }}">&nbsp;{{ member.email }}</a><br/>		
		{%- endif %}  
		{%- if member.phone != null and member.phone != "" %}
			<span class="glyphicon glyphicon-phone-alt"></span><a href="callto:{{ member.phone }}">&nbsp;{{ member.phone }}</a><br/>
		{%- endif %}  
		{%- if member.fax != null and member.fax != "" %}
			<span class="glyphicon glyphicon-print"></span>&nbsp;{{ member.fax }}   
		{%- endif %}
		</p>
	</div>
	{%- cycle 'close rows_members' : '', '', '', '</div>' %}
{%- endfor %}
{% cycle 'close rows_members' : '', '</div>', '</div>', '</div>' %}        
<hr/>    
<div class="wow bounceInDown" data-wow-offset="0" data-wow-delay="0.3s">
	<h2>Visitors</h2>
</div>
{%- for visitor in site.data.people.group_visitors %}
	{%- cycle 'add rows_visitors' : '<div class="row">', '', '', '' %}
	<div class="col-md-3">
		{%- if visitor.image_path != null and visitor.image_path != "" %}
			<img src="{{ visitor.image_path | prepend: site.baseurl }}" class="img-circle" alt="">	
		{%- else %}			
			<img src="{{ "/assets/images/people/blank_man.png" | prepend: site.baseurl }}" class="img-circle" alt="">	
		{%- endif %}  
		{%- if visitor.url != null and visitor.url != "" %}
		<h4><a href="{{visitor.url}}" target="_blank">{{visitor.name}}</a></h4>		
		{%- else %}	
		<h4>{{visitor.name}}</h4>		
		{%- endif %} 
		{%- if visitor.info != null and visitor.info != "" %}
			<p>{{visitor.post}}<br/>		
		{%- endif %}  
		{%- if visitor.email != null and visitor.email != "" %}
			<span class="glyphicon glyphicon-envelope"></span><a href="mailto:{{ visitor.email }}">&nbsp;{{ visitor.email }}</a><br/>		
		{%- endif %}  
		{%- if visitor.phone != null and visitor.phone != "" %}
			<span class="glyphicon glyphicon-phone-alt"></span><a href="callto:{{ visitor.phone }}">&nbsp;{{ visitor.phone }}</a><br/>
		{%- endif %}  
		{%- if visitor.fax != null and visitor.fax != "" %}
			<span class="glyphicon glyphicon-print"></span>&nbsp;{{ visitor.fax }}   
		{%- endif %} 
		</p>   
	</div>
	{%- cycle 'close rows_visitors' : '', '', '', '</div>' %}
{%- endfor %}
{%- cycle 'close rows_visitors' : '', '</div>', '</div>', '</div>' %}    
 <hr/>
	<div class="wow bounceInDown" data-wow-offset="0" data-wow-delay="0.3s">
		<h2>Former Group Members</h2>
	</div>
</div>
{%- for f_member in site.data.people.former_group_members %}
	{%- cycle 'add rows_f_member' : '<div class="row">', '', '', '' %}
	<div class="col-md-3">
		{%- if f_member.url != null and f_member.url != "" %}
		<h5><a href="{{f_member.url}}" target="_blank">{{f_member.name}}</a></h5>		
		{%- else %}	
		<h5>{{f_member.name}}</h5>		
		{%- endif %}  	              
	</div>
    {%- cycle 'close rows_f_member' : '', '', '', '</div>' %}
{%- endfor %}
{%- cycle 'close rows_f_member' : '', '</div>', '</div>', '</div>' %}  
<br/>