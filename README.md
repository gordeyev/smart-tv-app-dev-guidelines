# Smart TV app development guidelines

---

Smart TV App Development examples, tutorials, best-practices and documentation.

_(nice intro needed…)_

---

## Contents


* [LG](#lg)
	* [TV Specifications](#tv-specifications)
	* [Design Guidelines](#design-guidelines)
	* [Other](#other)
* [Samsung](#samsung)


---

## LG

Developer site: http://developer.lge.com/

Forum: [LG Official Forum][LG1]

**Documentation Link:** [http://developer.lgappstv.com/TV_HELP/index.jsp](http://developer.lgappstv.com/TV_HELP/index.jsp)

I find myself searching the documentation far too often, so here's the most important stuff so far. Feel free to make suggestions.

### TV Specifications

General Link: [source][LG2]

**Protocols**

All three models (NetCast 2.0 (2011), NetCast 3.0 H12 (2012), NetCast 3.0 M12 (2012)) support the following protocols:

* HTML file transportation: HTTP, HTTPS
* VoD media file transportation: MMSH, HTTP, RTMP, RTMPE
* Linear or live broadcasting: HLS, Widevine

[source][LG3]

**CODEC & Container**

mp4, wmv, asf, mov, wvm, avi, ts, mp3, wma

[source][LG4]

**MIME Types**

* general supported media - application/x-netcast-av
* Device Information - application/x-netcast-info
* WMV (ASF) - video/x-ms-asf, video/x-ms-wmv
* WMA - audio/x-ms-wma
* MP3 - audio/mpeg, audio/mp3
* MP4 - video/mp4, video/mpeg
* m3u8 - application/vnd.apple.mpegurl

[source][LG5]

**HTML5 Specifications**

Audio & Video tags supported and most Video events also supported.

[source][LG6]

### Design Guidelines

… to-do

### Other

LG Smart TV models list: http://www.lg.com/uk/smart-tvs

LG Smart TV for development suggestion: [32LM620T][LGlast]

[LG1]: http://developer.lge.com/community/forums/RetrieveForumList.dev?prodTypeCode=TV

[LG2]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FSpecifications.htm

[LG3]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FProtocols.htm

[LG4]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FSpecifications.htm

[LG5]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FAnnex+A+Complete+List+of+Supported+MIME+Types.htm

[LG6]: http://developer.lgappstv.com/TV_HELP/index.jsp?topic=%2Flge.tvsdk.developing.book%2Fhtml%2FDeveloping+Web+App%2FDeveloping+Web+App%2FAnnex+F+HTML5+Specifications.htm

[LGlast]: http://www.amazon.co.uk/LG-32LM620T-32-inch-Widescreen-Freeview/dp/B007IYW1A8/ref=sr_1_1?ie=UTF8&qid=1355338716&sr=8-1

---

## Samsung

(..)

> _last update: 12/12/2012_
