# bdfd-image-api
Image generation api for bdfd. I do not own any of these codes. It may or may not work as intended, haven't checked.
"Doesn't work anymore"

````````````````````````````````````````````````````````````




API 1 (Donald Trump Tweet):
Command: !dtt
Lang: BDScript Unstable

Code:
$nomention
$title[Donald Trump Tweeted]
$image[https://api.no-api-key.com/api/v2/trump?message=$replaceText[$message; ;%20;-1]]
$color[$random[0;999999]]
$argsCheck[>1;What you want to tweet by Donald Trump.]
$footer[Requested by $username]
$addTimestamp
$botTyping
$suppressErrors[Error Occurred; Please try again later.]
$deletecommand
$ignoreTriggerCase
$footerIcon[$authorAvatar]

````````````````````````````````````````````````````````````
````````````````````````````````````````````````````````````

API 2 (Random Car Pics With Details):
Command: !cars
Lang: BDScript Unstable

Code:
$nomention
$suppressErrors[The API is down, wait for a few minutes and try again]
$httpGet[https://api.popcat.xyz/car]
$title[$httpResult[title]]
$description[Image not loading? [Click here]($httpResult[image])]
$image[$httpResult[image]]
$footer[Requested by $username]
$color[00FFFF]

````````````````````````````````````````````````````````````
````````````````````````````````````````````````````````````

API 3 (Tweet But With Your PFP):
Command: !tweet
Lang: BDScript Unstable

Code:
$nomention
$onlyIf[$mentioned[1]==;]

$image[https://api.willz.repl.co/image/tweet?image=$authorAvatar&text=$replaceText[$message; ;+;-1]&username=$replaceText[$username; ;+;-1]]
$color[$random[1;16777216]]

````````````````````````````````````````````````````````````
````````````````````````````````````````````````````````````

API 4 (Pablo):
Command: !pablo
Lang: BDScript Unstable

Code:
$nomention
$image[https://api.berk404.ga/pablo?text=$replaceText[$message; ;+;-1]]

````````````````````````````````````````````````````````````
````````````````````````````````````````````````````````````

API 5 (CoinFlip):
Command: !coinflip
Lang: BDScript Unstable

Code:
$nomention
$title[You got $httpResult[coin]!]
$image[$httpResult[gif]]
$color[8b0000]
$footer[Requested by $username] 
$httpGet[https://www.no-api-key.com/api/v1/coin-flip]
$botTyping
$thumbnail[$httpResult[image]]
$addTimestamp
$footerIcon[$authorAvatar]

