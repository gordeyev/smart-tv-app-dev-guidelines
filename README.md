# Smart TV app development guidelines

---

Smart TV App Development examples, tutorials, best-practices and documentation.

_(nice intro needed…)_

---

### Contents

* [Devices](#devices)

* [Platforms / SDKs](#platformsandskds)

* [Media Specs](#media-specs)

* [Design guidelines](#design-guidelines)

* [Deployment and Testing](#deployment-and-testing)

* [Store Submission](#store-submission)

---

## Devices

### Samsung Devices ###

(_TO-DO_)

### LG Devices ###

LG Smart TV models list: [http://www.lg.com/uk/smart-tvs](http://www.lg.com/uk/smart-tvs)

LG Smart TV for development suggestion: [32LM620T](http://www.amazon.co.uk/LG-32LM620T-32-inch-Widescreen-Freeview/dp/B007IYW1A8/ref=sr_1_1?ie=UTF8&qid=1355338716&sr=8-1)

## Platforms and SDKs

This is the big picture with links for fast access of Smart TV Platforms and respective SDKs.

| Platform | Website | Documentation | Forum | SDK |
| -------- | :-----: | :-----------: | :---: | :-: |
| Android TV | [developer.android.com/tv](https://developer.android.com/tv)	| [Building Apps for TV](https://developer.android.com/training/tv/index.html) | - | [Android SDK](https://developer.android.com/sdk) |
| LG | [developer.lgappstv.com](http://developer.lgappstv.com/) | [TV Help](http://developer.lgappstv.com/TV_HELP/index.jsp) | [LG Developer Forums](http://developer.lge.com/community/forums/RetrieveForumList.dev?prodTypeCode=TV) | [Resources](http://developer.lge.com/resource/tv/RetrieveSdktools.dev) |
| NetTV (Sharp, Philips) | [yourappontv.com](http://yourappontv.com) | (Login required) | (Login required) | (Login required) |
| Opera TV | [operasoftware.com/opera-tv](http://www.operasoftware.com/opera-tv) | [dev.opera.com/tv](https://dev.opera.com/tv/) | [Opera TV Store Forums](http://forums.opera.com/categories/en-opera-tv-store) | [Opera TV Emulator](http://www.operasoftware.com/products/tv-emulator) |
| Roku | [roku.com/developer](https://www.roku.com/developer) | (Login required) | (Login required) | (Login required) |
| Samsung | [samsungdforum.com](http://www.samsungdforum.com) | [Development Guide](http://www.samsungdforum.com/Guide/) | [English Forum](http://www.samsungdforum.com/SamsungDForum/ForumDashBoard/c305cb96c72a9e5b) | [SDK Download](http://www.samsungdforum.com/Devtools/SdkDownload) |
| SmartTV Alliance (LG, Sharp, Philips) | [smarttv-alliance.org](http://smarttv-alliance.org)| [SDK Documentation](https://developers.smarttv-alliance.org/sdk-documentation) | [Forum](https://developers.smarttv-alliance.org/forum) | [SDK Overview](https://developers.smarttv-alliance.org/sdk-overview) |
| Yahoo Connected TV | [developer.yahoo.com/connectedtv/](https://developer.yahoo.com/connectedtv/) | - | - | - |

## Media Specs (Protocols and Codecs)

### LG

[LG Media Specs official documentation](http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FSpecifications.htm)

NetCast 2.0 (2011), NetCast 3.0 H12 (2012), NetCast 3.0 M12 (2012) support the following protocols:

> HTML file transportation: HTTP, HTTPS
>
> VoD media file transportation: MMSH, HTTP, RTMP, RTMPE
Linear or live broadcasting: HLS, Widevine

And the following Codecs/Containers:

> mp4, wmv, asf, mov, wvm, avi, ts, mp3, wma

HTML5 Audio and Video tags supported.<br />
Most HTML5 Video events also supported.

**MIME Types**

In order to play media in LG Smart TVs is necessary to use a media object.

	<object type="application/x-netcast-av" data="" autostart="false" width="500" height="500" id="lgPlayer" style="position:absolute; top:0px; left:0px; z-index: 1;"></object>
	
The `data` attribute is the video source and can be changed using Javascript to play supported media.

`type` attributes that can be used are:

> application/x-netcast-av (general supported media)<br />
> video/x-ms-asf, video/x-ms-wmv (WMV (ASF))<br />
> audio/x-ms-wma (WMA)<br />
> audio/mpeg, audio/mp3 (MP3)<br />
> video/mp4, video/mpeg (MP4)<br />
> application/vnd.apple.mpegurl (m3u8)

Useful official documentation links about these topics:

* [Protocols](http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FProtocols.htm)
* [Specifications](http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FSpecifications.htm)
* [MIME Types](http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FAnnex+A+Complete+List+of+Supported+MIME+Types.htm)
* [HTML5 support](http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FAnnex+F+HTML5+Specifications.htm)


## Design Guidelines

(_TO-DO_)


## Deployment and Testing

### Samsung

(_TO-DO_)

### LG

#### Real TV

[LG Deployment official documentation](http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.testing.book%2Fhtml%2FRealTV%2FDeploying+and+Testing+App+on+Real+TV%2FDeploying+and+Testing+App+on+Real+TV.htm)

Use the "Export App Test" option in the LG IDE and upload the package to the "App Test" option in the LG Developer site and download the DRM applied file. You create lgapps/installed/{appid} folder structure inside a usb stick, unzip the downloaded file into it and insert the usb stick into the LG TV.

When you upload the web app into the LG Developer site, you have to insert an URL in the form. This is really good, because it means that you don't have to go over this process every time you change something in your app.

So, I just create and upload a package that allows the TV to connect to my web server. After that I can continue/start to code the app and instantly test on the real device by reloading the TV app.

#### Emulator

[LG Testing on Emulator official documentation](http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.testing.book%2Fhtml%2FEmulator%2FTesting+App+on+Emulator%2FTesting+App+on+Emulator.htm)


## Store submission

### Samsung

<!-- Samsung Store submission is managed in the -->

**App Icons & Screenshots**

Icon Images for TV* Your icon image must be 512 x 423, SQUARE and at least 72 DPI
Your screenshot images must be 960 x 540, 1280 x 720 or 1920 x 1080 pixels and at least 72 DPI
Please upload an image less than 500 KB.

* JPG format only.

* Screenshot images must be 960 x 540, 1280 x 720 or 1920 x 1080 pixels.

### LG

LG Store submission is managed in the [LG Seller Lounge](http://seller.lgappstv.com/).<br />
It is important to read the "Seller Lounge Guide", easily spotted once you log in.

**Required Documents for App Submission**

Two documents are mandatory for submiting an app:

> AppDescription (appdescription.ppt)
>
> Self-Evaluation Checklist (app_self_evaluation_checklist.xls)

Download: [Required Documents for Application Submission to LG Seller Lounge](http://developer.lge.com/resource/tv/RetrieveDocReferencesList.dev) -> "documents for app qa.zip"

**App Icons & Screenshots**

[LG App Icon and Screenshot Guidelines (v4.1) [PDF]](http://developer.lge.com/resource/tv/RetrieveDocReferencesList.dev)

Exactly one icon is mandatory and needs to be accourdingly to these rules:

> 200 * 200
>
> PNG, JPG or GIF
>
> Max size: 100kb

At least two screenshots, as per:

> 1280 * 720 (browser, plex) or 960 * 540 (flash)
>
> PNG, JPG or GIF
>
> Max size: 200kb
>
> Max number of screenshots = 6

---

_last update: 11/02/2015_