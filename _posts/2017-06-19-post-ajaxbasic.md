---
layout: post
title : "java ajax basic"
tags:
  - java
  - javascript
  - JQuery
---



##인터넷 버전을 체크하는 자바스크립트

>아래와 같이 작성하면 괄호속에서 IE버전이 11보다 낮은경우가 걸러진다.

```javascript

var ajax = function () {
			
			$.ajax({
				type: 'POST', // POST 로 전송
				dataType: 'text json', // JSON 타입이 아닐경우 제거
				contentType: 'application/json; charset=utf-8',
				url: '.../url', // 호출 URL
				data: JSON.stringify({
					'key1': 'value1', "key2": "value2"
				}), // 파라메터 정보 전달,
				cache: false,
				success: function (data) {
					var jsonObj = JSON.parse(data.List);
					if (data.result == "SUCS") {
						if (data.List == "" || data.List == null || data.List == "null")
						{
							return;
						}
						else
						{
							if (jsonObj.Table.length > 0) {
								$.each(jsonObj.Table, function (index, item) {
                                } 
                                // each 종료
                            }
                        }
                    }
                }
              })
            }
```
            
