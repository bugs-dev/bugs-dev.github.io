---
layout: post
title:  "캐시 성능향상을 위한 시도"
description: 캐시 성능향상을 위해 대기시간, 다수요청처리 등의 문제점 개선
date:   2020-03-05 00:00:00
categories: java
authore: ybkim
---

# 캐시 성능향상을 위한 시도



## 목차

1. 동기식의 문제점
2. CacheManager
3. 끝



## 동기식의 문제점

일반적인 캐시의 사용법은,  
자주 사용되거나 긴 처리시간을 요구하는 코드부분을 정하고, 고유한 키와 만료시간을 부여하여,  
해당코드의 실행결과를 캐시에 저장하고 만료시간 안에는 코드의 실행대신 캐시를 사용하는 것으로 처리성능을 향상시키는 것.

여기서 문제점은  

* 캐시가 정기적으로 만료되어 갱신되는 시간에는 캐시생성 시간만큼의 대기시간이 필요
* 캐시만료 순간에 집중되는 다수의 요청으로 인해서 동일한 키와 동일한 결과를 반환하는 다수의 캐시생성 시도도 역시 발생
   
위의 원인으로 만료시간마다 처리 리소스가 증가하게 됨.


## CacheManager

CacheManager는 코드와 캐시요청 사이에서 캐시의 갱신과 다수요청에 대한 제어를 처리.  
--그럴듯한 그림--


*[ㅇㅀㅇㅀ]*

https://music.bugs.co.kr


**[ㅇㅀㄴㅇㄹㄴㄹㅇㅇㅀ]**

# 가나다라

>ㄴㅇㄹㄶㄴㅇㄹㄴㅇㄹ
>ㄴㅇㄹㄴㅇㄹㄴㅇㄹㄴㅇㄹ
>sbcd
>ㄴㅇㄹ

#### Inline code

`$ npm install marked`

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

---

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell 


비동기 적용

장점

단점


#### Javascript

```javascript
const express = require('express')
const app = express()
 
app.get('/', function (req, res) {
  res.send('Hello World')
})
 
app.listen(3000)
```
