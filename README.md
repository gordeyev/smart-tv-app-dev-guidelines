# Smart TV app development guidelines

---

Smart TV App Development examples, tutorials, best-practices and documentation.

_(nice intro needed…)_

---

### Contents

* [Devices](#devices)

* [Media Specs](#media-specs)

* [Design guidelines](#design-guidelines)

* [Dev Resources](#dev-resources)

* [Deployment and Testing](#deployment-and-testing)

* [Store Submission](#store-submission)

---

## Devices

### Samsung Devices ###

Samsung Smart TV models list: [http://www.samsung.com/us/video/tvs/all-products](http://www.samsung.com/us/video/tvs/all-products)

Samsung Smart TV for development suggestion: [UE32H5500](http://www.amazon.co.uk/Samsung-UE32H5500-32-inch-Widescreen-Freeview/dp/B00JOKEGOS)


#### Browser User-Agent String Format

| Year | UA String |
| :--: | :------- |
| 2015 | Mozilla/5.0 (SMART-TV; Linux; Tizen 2.3) AppleWebkit/538.1 (KHTML, like Gecko) SamsungBrowser/1.0 TV Safari/538.1 |
| 2014 | Mozilla/5.0 (SMART-TV; X11; Linux armv7l) AppleWebkit/537.42 (KHTML, like Gecko) Safari/537.42 |
| 2013 | Mozilla/5.0 (SMART-TV;X11; Linux i686) AppleWebkit/535.20+ (KHTML, like Gecko) Version/5.0 Safari/535.20+ |
| 2012 | Mozilla/5.0 (SMART-TV; X11; Linux i686) AppleWebKit/534.7 (KHTML, like Gecko) Version/5.0 Safari/534.7 |
| 2011 | Mozilla/5.0 (SmartHub; SMART-TV; U; Linux/SmartTV) AppleWebKit/531.2 (KHTML, like Gecko) Web Browser/1.0 SmartTV Safari/531.2+ |

@source: [http://developer.samsung.com/technical-doc/view.do?v=T000000203](http://developer.samsung.com/technical-doc/view.do?v=T000000203)

### LG Devices ###

LG Smart TV models list: [http://www.lg.com/uk/smart-tvs](http://www.lg.com/uk/smart-tvs)

LG Smart TV for development suggestion: [32LM620T](http://www.amazon.co.uk/LG-32LM620T-32-inch-Widescreen-Freeview/dp/B007IYW1A8/ref=sr_1_1?ie=UTF8&qid=1355338716&sr=8-1)

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
* [HTML5 support](http://developer.lgappstv.com/TV_HELP/topic/lge.tvsdk.developing.book/html/Developing%20Web%20App/Developing%20Web%20App/Supported%20HTML5%20CSS3%20Standard%20for%20the%20NetCast%20Platform%20and%20Emulator.htm?path=1_2_2#_Toc455136510)


## Design Guidelines

* [LG Netcast icon & screenshot guide](http://developer.lge.com/resource/tv/RetrieveDocReferencesContent.dev?resourceId=RS00000751)
* [LG Netcast ui guide](http://developer.lge.com/resource/tv/RetrieveDocReferencesContent.dev?resourceId=RS00000737)
* [WebOS UX checklist](http://developer.lge.com/webOSTV/design/ux-checklist/)
* [Samsung guide](http://www.samsungdforum.com/UxGuide/)
* [Tizen guide](http://www.samsungdforum.com/TizenUxGuide)
* [Tizen checklist](http://www.samsungdforum.com/TizenUxGuide/09/09_uxchecklist.html)
* "Designing for TV" - Developer Android - [http://developer.android.com/training/tv/index.html](http://developer
.android.com/training/tv/index.html)

## Dev Resources

Useful resources for Smart TV Apps development.

### Platforms and SDKs

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

### Frameworks

* _\*shameless\*_ smart-tv.js - Smart TV Development Framework - [https://github.com/ruiposse/smart-tv.js](https://github.com/ruiposse/smart-tv.js)

* TV Application Layer (BBC) - [http://fmtvp.github.io/tal/](http://fmtvp.github.io/tal/) - [https://github.com/fmtvp/tal](https://github.com/fmtvp/tal)

* ZombieBox - Cross-platform SmartTV/STB Javascript framework - [http://zombiebox.net](http://zombiebox.net)

* Metrological Application Framework 3.0 - [https://github.com/Metrological/maf3-sdk](https://github.com/Metrological/maf3-sdk)

* Mautilus Smart TV SDK - [http://smarttv.mautilus.com/SDK/](http://smarttv.mautilus.com/SDK/)

* Enyo Javascript Framework [https://github.com/enyojs](https://github.com/enyojs)

* Joshfire Framework - [https://github.com/joshfire](https://github.com/joshfire)

### Code

* "generator-smarttv - Yeoman generator to scaffold a Samsung SmartTV app" -[https://github.com/eddiemoore/generator-smarttv](https://github.com/eddiemoore/generator-smarttv)
* Gridy.js - [https://github.com/ialpert/gridy.js/](https://github.com/ialpert/gridy.js/) - [http://ialpert.github.com/gridy.js](http://ialpert.github.com/gridy.js)
* "Samsung SmartTv Packager (2013)" - [https://github.com/imgntn/samsung-smartTV-packager](https://github.com/imgntn/samsung-smartTV-packager)
* Debugging server (Samsung Smart TV)- [https://gist.github.com/janmonschke/4992216](https://gist.github.com/janmonschke/4992216)
* Basic Smart TV App Server - [https://github.com/rposbo/basic-smart-tv-app-server](https://github.com/rposbo/basic-smart-tv-app-server)
* "Samsung sample Brightcove video player" - [https://github.com/BrightcoveOS/Samsung-Smart-TV-Sample-App](https://github.com/BrightcoveOS/Samsung-Smart-TV-Sample-App)
* 'Polyfill for localStorage in Smart TV' - [https://github.com/artempoletsky/Smart-LS](https://github.com/artempoletsky/Smart-LS)


### Articles / Blog posts / Stackoverflow

###### Articles

* "Smart TV Hacking" - [http://www.delaat.net/rp/2012-2013/p39/report.pdf](http://www.delaat.net/rp/2012-2013/p39/report.pdf)

###### Blog Posts

* [http://eddie-moore.com/2014/01/samsung-smart-tv-app-generator-for-yeoman](http://eddie-moore.com/2014/01/samsung-smart-tv-app-generator-for-yeoman)
* [http://robinosborne.co.uk/2013/02/04/year-of-101s-february-samsung-smart-tv](http://robinosborne.co.uk/2013/02/04/year-of-101s-february-samsung-smart-tv)
* [http://robinosborne.co.uk/2013/02/11/smart-tv-101-part-2-app-development](http://robinosborne.co.uk/2013/02/11/smart-tv-101-part-2-app-development)
* [http://robinosborne.co.uk/2013/02/14/smart-tv-101-part-3-deploying-to-tv](http://robinosborne.co.uk/2013/02/14/smart-tv-101-part-3-deploying-to-tv)
* [http://robinosborne.co.uk/2013/02/28/samsung-smart-tv-part-4-creating-packages-without-the-sdk](http://robinosborne.co.uk/2013/02/28/samsung-smart-tv-part-4-creating-packages-without-the-sdk)

###### Stackoverflow

* "SmartTV development for starters" - [http://stackoverflow.com/questions/12940572/smarttv-development-for-starters](http://stackoverflow.com/questions/12940572/smarttv-development-for-starters)

### Slides, Talks and Presentations

(_TO-DO_)

## Deployment and Testing

### Samsung

#### Change TV Region

```
Disclaimer:

I take no responsability for any damage to your television
or any other issues that may arise from following these tutorials.

I do not recommend purchasing a Samsung Smart TV to access
streaming services from another country.

PROCEED AT YOUR OWN RISK!

You may also need some VPN connection after changing your
TV store in order for some apps to work properly.
```

Tutorials:

* **D-Series** and **E-Series**

1. Make sure your television is connected to the internet. If you require help, consult your television’s manual.
2. Power up your TV and enter the smart hub by pressing the appropriate key on the Samsung remote.
3. Once the Smart Hub has appeared, press only the following keys in exactly this order:
	* Fast-forward (>>)
	* 289
	* Rewind (<<)
4. If the key-press sequence was performed correctly, you should have entered a backdoor service menu. A list of countries, representing the various regional app stores will appear so you can now select the one that you wish to use.
5. After a short moment, you will be asked to update the Smart Hub. Press Yes.
6. The Smart Hub will automatically remove all existing apps and install different ones from the new store. I recommend rebooting the television and agreeing to any further smart hub updates. It is up to you to choose which additional apps you wish to install.


@source: [http://www.eyeondemand.com/2013/02/07/how-to-changing-your-samsung-tvs-country-app-store/](http://www.eyeondemand.com/2013/02/07/how-to-changing-your-samsung-tvs-country-app-store/)

* **F-Series (2013)** and **H-Series (2014)**

Guide with pictures: [http://support-us.samsung.com/cyber/popup/iframe/pop_troubleshooting_fr.jsp?idx=428339](http://support-us.samsung.com/cyber/popup/iframe/pop_troubleshooting_fr.jsp?idx=428339)

1. Set the TV to the TV source, press the source button and use the navigation pad, select TV and then click to select.
2. Open the Main Menu.
3. Use the navigational pad to select the System portion of the Main Menu, and then click to enter the sub menu.
4. Setup will be selected by default, click to begin the setup.
5. You will begin the on-screen setup that you completed when you first bought the television. Your previously entered information will be retained.
6. Continue through the on-screen setup until you arrive at the Smart Hub Terms & Conditions, Privacy Policy page in the on-screen setup.
7. With the Smart Hub Terms & Conditions, Privacy Policy page up on the TV press the following buttons in sequential order.
![alt text](http://wiki.samygo.tv/images/9/9a/F-series-samsung-change-region-guide.jpg "Samsung change region guide.")
8. The country list will appear. Select your country from the list and then click to continue.
9. Complete the on-screen setup. You TV's country code has now been changed.

@source: [http://wiki.samygo.tv/index.php5/How_To_Set_Your_Country_Code_In_Smart_Hub](http://wiki.samygo.tv/index.php5/How_To_Set_Your_Country_Code_In_Smart_Hub)

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

Icon Images for TV

* Your icon image must be 512 x 423, SQUARE and at least 72 DPI
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

_last update: 27/03/2015_
