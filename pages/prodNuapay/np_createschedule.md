---
title: Create Payment Schedule
keywords: Create Payment Schedule
summary: "Create Payment Schedule RESTful API"
sidebar: np_sidebar
permalink: np_createschedule.html
folder: prodNuapay
toc: false
---

## API Details

The Create Payment Schedule request allows you to create either a Fixed-Length or an Open-Ended schedule. 

The fixed-length schedule will result in a number of Direct Debit payments being created; an open-ended schedule will generate a single Direct Debit (with additional single payments being added as required, based on the configured frequency of the payments).



<ul id="profileTabs" class="nav nav-tabs">
    <li class="active"><a href="#profile" data-toggle="tab">Request</a></li>
    <li><a href="#about" data-toggle="tab">Response</a></li>
   
</ul>
  <div class="tab-content">
<div role="tabpanel" class="tab-pane active" id="profile">


  <table>
<colgroup>
<col width="30%" />
<col width="90%" />
</colgroup>

<tbody>
<tr>
<td markdown="span">Usage</td>
<td markdown="span">You can only create a schedule against an Active mandate</td>
</tr>
<tr>
<td markdown="span">Method</td>
<td markdown="span"><span class="label label-info">POST </span>
</td>
</tr>
<tr>
<td markdown="span">URI</td>
<td markdown="span">/schemes/{CS_ID}/mandates/{MANDATE_ID}/paymentschedules
</td>
</tr>
<tr>
<td markdown="span">Required Arguments</td>
<td markdown="span">paymentFrequency, paymentType, startDate, paymentAmount (Other arguments may be required depending on your schedule requirements (for example if you are setting up a FIXED_LENGTH schedule then the numberOfPayments is required).)
</td>
</tr>
</tbody>
</table>



</div>

<div role="tabpanel" class="tab-pane" id="about">
<p>A successful request will return a <b>201 Created</b> response code</p>
<p>The following is the complete list of possible status codes, which may be returned in the response:</p>
    {% include httpcodes.html %}
    
 
    </div>


</div>

{% include swaggerlink.html %}

{% include links.html %}
