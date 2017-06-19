---
layout: post
title : "java ajax basic"
tags:
  - java
  - javascript
  - JQuery
---



**인터넷 버전을 체크하는 자바스크립트

ajax의 기본틀 해당틀을 복사해서 사용한다면 편리하다.

대부분의 기본적인 세팅이 다 되어있게 작성하였다.

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
            
