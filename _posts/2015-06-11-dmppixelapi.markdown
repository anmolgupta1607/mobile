---
layout: nav
title:  "DMP Pixel API"
---

<h6>DMP</h6>

Data Management Platform helps in Collection and storage of User Centric data in a permanent data store. These Data is used in delivering tailored Ads to the users thery bring in more conversions through Ad delivery. 

A Parameter is passed from the URL that specifies the number of ads/creatives returned.

<strong>Resource URL:</strong>

http://test.snapdeal.com/pixel?prod_id/category/campaign_id/creative_id/action/impressions_served/converted/last_purchase_category/idfa/customer_ltv/exchanges/oid/w/e/p/pval/adv/page/asid/sid/ip/key/aid/price

<h6>Resource Information:</h6>

<strong>Response:</strong> The cookie id is generated and stored in RocksDB 

<strong>Method:</strong> GET



<h6>Input Parameters</h6>

<table class="table">
<th>Parameter Name</th>
<th>Details</th>
<th>Required</th>

<tr>
<td>prodid</td>
<td>Unique ID for a Product</td>
<td>Optional</td>
</tr>

<tr>
<td>Category</td>
<td>Category page in which the user is in</td>
<td>Optional</td>
</tr>

<tr>
<td>Creative_id</td>
<td>The Ad/Creative viewed/clicked by the user</td>
<td>Optional</td>
</tr>

<tr>
<td>Action</td>
<td>The action performed by the user(varies from 1-10)</td>
<td>Yes</td>
</tr>

<tr>
<td>Impression_served</td>
<td>The impression id served to the user</td>
<td>Optional</td>
</tr>

<tr>
<td>Converted</td>
<td>This field is set when the user gets converted through an Ad</td>
<td>Optional</td>
</tr>

<tr>
<td>Customer_ltv</td>
<td>The filed denotes the Customer Life Time Value</td>
<td>Optional</td>
</tr>

<tr>
<td>Exchange</td>
<td>The SSP from which the request arrived</td>
<td>Optional</td>
</tr>

<tr>
<td>OrderId</td>
<td>The unique order id if a purchase happens</td>
<td>Optional</td>
</tr>

<tr>
<td>w</td>
<td>The website name from which the ad came</td>
<td>Optional</td>
</tr>

<tr>
<td>w</td>
<td>The website name from which the ad came</td>
<td>Optional</td>
</tr>

<tr>
<td>e</td>
<td>The email id of the user if the user is logged in</td>
<td>Optional</td>
</tr>

<tr>
<td>pval</td>
<td>The value of the product if a purchase happens</td>
<td>Optional</td>
</tr>

<tr>
<td>advid</td>
<td>The advertiser Id if the user purchased a product through an Ad delivery</td>
<td>Optional</td>
</tr>

<tr>
<td>page</td>
<td>The Page type in which the user is present</td>
<td>Optional</td>
</tr>

<tr>
<td>adspaceid</td>
<td>The adspace in which the ad is delivered</td>
<td>Optional</td>
</tr>

<tr>
<td>key</td>
<td>The search key if the user has performed a search option</td>
<td>Optional</td>
</tr>

<tr>
<td>ip</td>
<td>The Ip address of the user</td>
<td>Yes</td>
</tr>

<tr>
<td>Device id</td>
<td>Unique Id for the device</td>
<td>Yes</td>
</tr>

<tr>
<td>Device type</td>
<td>The device type may include type of mobile(ios,android)</td>
<td>Yes</td>
</tr>
</table>

 	 	 

<strong>Sample URL</strong>

http://209.237.236.37:9778/pixel?prod_id=test_pro1&category=tst_cat1&campaign_id=tst_cmp1&creative_id=tst_crtv1&action=1&impressions_served=tst&converted=tst&global_category=test_globl&last_purchase_category=tst_pcat&idfa=tst&customer_ltv=tst&exchanges=test&oid=1234&w=snapdeal.com&e=test@t.com&p=pub321&pval=123&adv=adv123&page=page12&asid=adsTest&sids=sidTest&ip=127.1&key=searchKey&aid=adid123&price=777

Note: The document that explains the list of action that can be performed by the  user and data collected when a particular action is performed is given below