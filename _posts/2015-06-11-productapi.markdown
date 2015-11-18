---
layout: nav
title:  "Product and Banner Ads API"
---

<h6>API for Product and Banner Ad serving</h6>


This API returns the creative information of a Product or Banner AD based on the ad space ID that is passed fro URL.

<strong>Resource URL:</strong>

http://test.snapdeal.com/pub/getAd?pub_id/ad_Space_ID/impressionid

<h6>Resource Information:</h6>

<strong>Response Format :</strong> JSON

<strong>Method:</strong> GET

<strong>Authentication:</strong> Optional

<h6>Input Parameters</h6>

<table class="table">
<th>Parameter Name</th>
<th>Details</th>
<th>Required</th>

<tr>
<td>pubid</td>
<td>Unique ID for the Publisher. For Snapdeal Inventory the default value is 1</td>
<td>Yes</td>
</tr>

<tr>
<td>js</td>
<td>Its a boolean Value that specifies whether JS tag is present</td>
<td>Optional</td>
</tr>

<tr>
<td>inv</td>
<td>This parameter denotes the type of inventory(App,msite or Website)</td>
<td>Optional</td>
</tr>

<tr>
<td>site id</td>
<td>Denotes the website from which the Ad request came(By default 101)</td>
<td>Optional</td>
</tr>

<tr>
<td>adspace id</td>
<td>Unique Id for the adspace/adslot in a particular page</td>
<td>Yes</td>
</tr>

<tr>
<td>impression id</td>
<td>Unique Id for the request</td>
<td>Yes</td>
</tr>

<tr>
<td>rs</td>
<td>Denotes the response type(HTML/JSON)</td>
<td>Optional</td>
</tr>

<tr>
<td>Category</td>
<td>The category type from which the request originated (Mobile/Fashion/Books)</td>
<td>Optional</td>
</tr>

<tr>
<td>Pagetype</td>
<td>The category type from which the request originated (Home/PDP/Thankyou)</td>
<td>Optional</td>
</tr>




</table>

 	 	 

<strong>Sample Request</strong>

GET

 http://test.snapdeal.com/pub/getAd?pubId=1&adSpaceId=1005&impressionid=12345

 
<strong>Sample Response</strong>

[
{
"adSpaceId": 1001,
"adId": 567567,
"campaignId": 334455,
"image_url": "http://ch.reducedata.com/rtb/getImage/1/567567?cb=886727616",
"requestId": "100111",
"pixel_url": "http://impression.reducedata.com/rtb/impressionPixel/1/567567/hello?cb=1606203778&vid=0&auid=${AUCTION_ID}",
"width": 300,
"advId": 2857,
"click_url": "http://click.reducedata.com/rtb/clickTracker/1/567567/hello?cb=1563693528&auid=${AUCTION_ID}",
"type": "CREATIVE_TYPE_BANNER_AD",
"height": 250,
"target": "_blank"
}
]

<h6>Output Parameters</h6>

<table class="table">
<th>Parameter Name</th>
<th>Details</th>
<th>Type</th>

<tr>
<td>offerPrice</td>
<td>Price at which product sold in Snpadeal site</td>
<td>Integer</td>
</tr>

<tr>
<td>creativeHeight</td>
<td>Height of the creative</td>
<td>Integer</td>
</tr>

<tr>
<td>pixel_url</td>
<td>Pixel URL of the creative</td>
<td>Url</td>
</tr>

<tr>
<td>sellerName</td>
<td>Name of the seller</td>
<td>String</td>
</tr>

<tr>
<td>rating</td>
<td>Seller Rating</td>
<td></td>
</tr>

<tr>
<td>discount</td>
<td>Percentage of discount offered</td>
<td>Integer</td>
</tr>

<tr>
<td>extClickTrackingUrl</td>
<td>When an Ad is delivered in third-party publisher site this URL is used

to track the click</td>
<td>URL</td>
</tr>

<tr>
<td>creativeId</td>
<td>Unique identifier of the creative</td>
<td>String</td>
</tr>

<tr>
<td>sellerCode</td>
<td>Unique seller code</td>
<td>String</td>
</tr>

<tr>
<td>extImpressionTrackingUrl</td>
<td>	

When an Ad is delivered in third-party publisher site this URL is used

to track the Impression</td>
<td>URL</td>
</tr>

<tr>
<td>clickTrackingUrl</td>
<td>Tracking of the clicked Url(R)</td>
<td>URL</td>
</tr>
<tr>
<tr>
<td>requestId</td>
<td>Id assigned to each unique request</td>
<td>String</td>
</tr>
<tr>
<td>price</td>
<td>Actual Price of the product</td>
<td>Integer</td>
</tr>
<td>conversionTrackingUrl</td>
<td>Url of the converted ads (click to buy)</td>
<td>URL</td>
</tr>
<tr>
<td>pogId</td>
<td>Product offer group id</td>
<td>String</td>
</tr>
<tr>
<td>height</td>
<td>hieght of the frame/ad</td>
<td>Integer</td>
</tr>
<tr>
<td>ratingNum</td>
<td>denotes the number of reviews for a Particular Product</td>
<td>Integer</td>
</tr>
<tr>
<td>altText</td>
<td>Text to be displayed</td>
<td>String</td>
</tr>
<tr>
<td>campaignId</td>
<td>Unique Id assigned to the campaign</td>
<td>String</td>
</tr>
<tr>
<td>image_Url</td>
<td>URL of the Image</td>
<td>String</td>
</tr>
<tr>
<td>creativeSize</td>
<td>size of the creative</td>
<td>-</td>
</tr>
<tr>
<td>creative</td>
<td>Denotes the type of the creative(Banner or Product)</td>
<td>String</td>
</tr>
<tr>
<td>target</td>
<td>Targeting Option enabled by the seller(Location,Segment)</td>
<td>String</td>
</tr>
<tr>
<td>creativeWidth</td>
<td>width of the creative</td>
<td>Integer</td>
</tr>
<tr>
<td>adSpaceId</td>
<td>Area defined for ad display</td>
<td>String</td>
</tr>
<tr>
<td>adId</td>
<td>Unique id assigned to the ad</td>
<td>String</td>
</tr>
<tr>
<td>creativeType</td>
<td>Type of creative:banner?</td>
<td>Integer</td>
</tr>
<tr>
<td>name</td>
<td>Name give to the ad</td>
<td>String</td>
</tr>
</table>

<strong>Requests to the above APIs will result in one of 3 possible return codes:</strong> 

<table class="table">
<tr>
	<td>404 – BAD REQUEST</td>
	<td>Returned if there is a parameter mismatch in terms of format.</td>
</tr>
<tr>
	<td>500 – SERVER EXCEPTION</td>
	<td>Returned in case of exceptions on the server. For example, a connections failure, etc.</td>
</tr>
<tr>
	<td>200 – OK</td>
	<td>Returned if the request was processed properly. </td>
</tr>


</table>