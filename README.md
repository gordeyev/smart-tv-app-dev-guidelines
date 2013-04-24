# Smart TV app development guidelines

---

Smart TV App Development examples, tutorials, best-practices and documentation.

_(nice intro needed…)_

---

## Contents


* [LG](#lg)
	* [Media Specs](#media-specs-protocols-and-codecs)
	* [LG SDK](#lg-sdk)
	* [Design Guidelines](#design-guidelines)
	* [Deployment](#deployment)
	* [Store submission](#store-submission)
	* [Other](#other)
* [Samsung](#samsung)


---


## LG

Developer site: http://developer.lge.com/

Forum: [LG Official Forum][LG1]

**Documentation Link:** [http://developer.lgappstv.com/TV_HELP/index.jsp](http://developer.lgappstv.com/TV_HELP/index.jsp)

I find myself searching the documentation far too often, so here's the most important stuff so far. Feel free to make suggestions.



### LG SDK

LG Software Development Kit consists in a VirtualBox image that contains the LG Emulator and RCU (Remote Control Unit).

**LG Smart TV SDK V3.0**

Release Date: 08-FEB-2013

Supported Platforms: Windows, Linux, Mac

Download: [LG SDK][LG-SDK-DOWNLOAD]



### Media Specs (Protocols and Codecs)

General official documentation [link][LG2].

All three models (NetCast 2.0 (2011), NetCast 3.0 H12 (2012), NetCast 3.0 M12 (2012) support the following protocols:

* HTML file transportation: HTTP, HTTPS
* VoD media file transportation: MMSH, HTTP, RTMP, RTMPE
Linear or live broadcasting: HLS, Widevine

And the following Codecs/Containers:

* mp4, wmv, asf, mov, wvm, avi, ts, mp3, wma

HTML5 Audio and Video tags supported. Most HTML5 Video events also supported.

**MIME Types**

In order to play media in LG Smart TVs is necessary to use a media object. Example:

	<object type="application/x-netcast-av" data="" autostart="false" width="500" height="500" id="lgPlayer" style="position:absolute; top:0px; left:0px; z-index: 1;"></object>
	
The "data" attribute can be changed using Javascript to play whatever supported media. The "type" attributes that can be used are:

* application/x-netcast-av - general supported media
* video/x-ms-asf, video/x-ms-wmv - WMV (ASF)
* audio/x-ms-wma - WMA
* audio/mpeg, audio/mp3 - MP3
* video/mp4, video/mpeg - MP4
* application/vnd.apple.mpegurl - m3u8

Here are some useful official documentation links about these topics:

* [Protocols][LG3]
* [Specifications][LG4]
* [MIME Types][LG5]
* [HTML5 support][LG6]



### Design Guidelines

(_TO-DO_)



### Testing

**Real TV**

First, use the "Export App Test" option in the LG IDE. Then, update the package to the "App Test" option in the LG Developer site and download the DRM applied file. You create lgapps/installed/{appid} folder structure inside a usb stick, unzip the downloaded file into it and insert the usb stick into the LG TV.

When you upload the web app into the LG Developer site, you have to insert an URL in the form. This is really good, because it means that you don't have to go over this process every time you change something in your app.

So, I just create and upload a package that allows the TV to connect to my web server. After that I can continue/start to code the app and instantly test on the real device by reloading the TV app.

It's always good to read the [official documentation about deployment][LG7].

**Emulator**

The best way to test an LG App is to have a local web server and to open the app link using the RCU.

Read the official documentation about [testing on Emulator][LG8].



### Store submission

LG Store submission is managed in the [LG Seller Lounge](http://seller.lgappstv.com/).

It is important to read the "Seller Lounge Guide", easily spotted once you log in.

***Required Documents for App Submission***

Two documents are mandatory for submiting an app:

* AppDescription (appdescription.ppt)

* Self-Evaluation Checklist (app_self_evaluation_checklist.xls)

Download: [Required Documents for Application Submission to LG Seller Lounge](http://developer.lge.com/resource/tv/RetrieveDocReferencesList.dev) -> "documents for app qa.zip"

***LG App icon & screenshots***

Exactly one icon is mandatory and needs to be accourdingly to these rules:

* 200 * 200
* PNG, JPG or GIF
* max size 100kb

At least two screenshots, as per:

* 1280 * 720 (browser, plex) or 960 * 540 (flash)
* PNG, JPG or GIF
* max size 200kb
* max number of screenshots = 6

Download: [LG Smart TV Guidelines for App Icon and Screenshot](http://developer.lge.com/resource/tv/RetrieveDocReferencesList.dev) -> "LG Smart TV Guidelines for App Icon and Screenshot_V4.1.pdf"



### Other

LG Smart TV models list: [http://www.lg.com/uk/smart-tvs](http://www.lg.com/uk/smart-tvs)

LG Smart TV for development suggestion: [32LM620T][LGlast]

[LG1]: http://developer.lge.com/community/forums/RetrieveForumList.dev?prodTypeCode=TV

[LG2]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FSpecifications.htm

[LG3]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FProtocols.htm

[LG4]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FSpecifications.htm

[LG5]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FAnnex+A+Complete+List+of+Supported+MIME+Types.htm

[LG6]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FAnnex+F+HTML5+Specifications.htm

[LG7]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.testing.book%2Fhtml%2FRealTV%2FDeploying+and+Testing+App+on+Real+TV%2FDeploying+and+Testing+App+on+Real+TV.htm

[LG8]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.testing.book%2Fhtml%2FEmulator%2FTesting+App+on+Emulator%2FTesting+App+on+Emulator.htm

[LG-SDK-DOWNLOAD]: http://developer.lge.com/resource/tv/RetrieveSdktools.dev

[LGlast]: http://www.amazon.co.uk/LG-32LM620T-32-inch-Widescreen-Freeview/dp/B007IYW1A8/ref=sr_1_1?ie=UTF8&qid=1355338716&sr=8-1

---



## Samsung

(...)

> _last update: 23/04/2013_
