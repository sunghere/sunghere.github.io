---
layout: post
title : "java script IE 버전 체크"
tags:
  - java
  - javascript
  - ie
---



##인터넷 버전을 체크하는 자바스크립트

>아래와 같이 작성하면 괄호속에서 IE버전이 11보다 낮은경우가 걸러진다.

```javascript
var IEVERSION = getInternetExplorerVersion();
var getInternetExplorerVersion = function() {
		var rv = -1;
			if (navigator.appName == 'Microsoft Internet Explorer') {
				var ua = navigator.userAgent;
				var re = new RegExp("MSIE ([0-9]{1,}[\.0-9]{0,})");
				if (re.exec(ua) != null)
					rv = parseFloat(RegExp.$1);
			}
			else if (navigator.appName == 'Netscape') {
				var ua = navigator.userAgent;
				var re = new RegExp("Trident/.*rv:([0-9]{1,}[\.0-9]{0,})");
				if (re.exec(ua) != null)
					rv = parseFloat(RegExp.$1);
			}
			return rv;
		}
			var useragent = navigator.userAgent;

			if (useragent.toUpperCase().indexOf("WINDOW") > 0 && IEVERSION < 11 && IEVERSION > -1) {
				
			}
```
