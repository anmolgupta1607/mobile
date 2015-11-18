---
layout: nav
title:  "Carousel Ads API"
---

<h6>API for Carousel Ad Display</h6>

Carousel ads allows you to show multiple images and links, letting you feature more images in a single advertisement. Below mentioned API returns multiple Ads(creatives) in a Carousel.

A Parameter is passed from the URL that specifies the number of ads/creatives returned.

<strong>Resource URL:</strong>

http://test.snapdeal.com/pub/getAd?pubId/adSpaceId/impressionId/multi

<h6>Resource Information:</h6>

<strong>Response Format :</strong> JSON

<strong>Method:</strong> GET



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

<tr>
<td>multi</td>
<td>This parameter denotes the number of ads to be displayed in the carousal</td>
<td>Yes</td>
</tr>


</table>

 	 	 

<strong>Sample Request</strong>

GET

http://209.237.251.142:9558/pub/getAd?pubId=1&adSpaceId=1212&impressionId=hello&multi=3

The method responds with three different creatives are returned in a single response. 

 
<strong>Sample Response</strong>

[
{
"offerPrice": 0,
"creativeHeight": 250,
"pixel_url": "http://impression.reducedata.com/rtb/impressionPixel/1/123123/hello?cb=315318047&vid=0&auid=${AUCTION_ID}",
"linkTarget": "",
"sellerName": "westcoseLTD",
"rating": 0,
"discount": 0,
"extClickTrackingUrl": "",
"extConversionTrackingUrl": "",
"creativeId": 123123,
"sellerCode": "S1001",
"extImpressionTrackingUrl": "",
"clickTrackingUrl": "",
"requestId": "11101",
"price": 1600,
"conversionTrackingUrl": "",
"click_pixel_url": "http://click.reducedata.com/rtb/clickTracker/1/123123/hello?cb=1357617445&auid=${AUCTION_ID}",
"click_url": "http://click.reducedata.com/rtb/clickTracker/1/123123/hello?cb=1357617445&auid=${AUCTION_ID}",
"pogId": 0,
"height": 250,
"ratingNum": 0,
"altText": "",
"campaignId": 112233,
"image_url": "http://ch.reducedata.com/rtb/getImage/1/123123?cb=85756826",
"clickThroughUrl": "",
"advId": 2857,
"impressionTrackingUrl": "",
"creativeSize": "720x250",
"creative": "",
"target": "_blank",
"creativeWidth": 720,
"adSpaceId": 1212,
"adId": 123123,
"creativeType": "CREATIVE_TYPE_PRODUCT_CAROUSEL_AD",
"name": "",
"isPixel": "",
"width": 720
} 

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
	
	
	