---
layout: post
title: "크롤링(crawling)의 도구 1 - BeautifulSoup"
tags: [crawling, study, beautifulsoup]
comments: true
---
크롤링은 데이터를 모으는 첫번째 방법이다. 가장 필요한만큼 많은 방법이 존재한다.
파이썬에서 크롤링을 하는 방법은 크게 세가지가 있다. 오늘은 가장 먼저 배우게 되는 BeautifulSoup에 대해 정리해보겠다.

필요한 모듈은 다음과 같다.
```
import requests
from bs4 import BeautifulSoup
```
네이버 뉴스를 한번 크롤링 해보자
검색 keyword를 NLP로 해보겠다.

![enter image description here](https://lh3.googleusercontent.com/21fDklf-ttwBdt4h14RtCTLNpyH51dVQvICbfKwW5XVa_kqCHkpr-4AVo2wFLkBqF5rOJV2tb_hF=s700)

검색어를 입력하고 '뉴스'탭에 들어가면 위와 같은 주소가 나온다. 
url 주소를 잘 뜯어보면 물음표 부호 뒤에 이것저것 써있다. 앞으로 저 물음표를 기준으로 본다.
물음표 기준으로 물음표 앞은 도메인, 뒤는 파라미터이다.
```
url = 'https://search.naver.com/search.naver'
keyword = 'nlp'
params = {'where':'news', 'query'= keyword}
resp = requests.get(url, params = params)
```
위와 같이 파라미터를 별도 지정해줄 수 있다. (여기서 'sm=tab_jum' 는 빠졌는데,  리퀘스트 보낼 때는 없어도 상관 없는 요소이다) 여기서 `resp.url`을 입력하면 해당 url이, `resp.status_code`를 입력하면 `200`이 뜬다. 200은 url이 정상적인 신호를 나에게 주고 있다는 뜻이다. (`'resp.ok`도 있는데, 정상적인 접속일 경우 `True`가, 에러가  을 경우 `False`가 뜬다.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg4NzgyNDY1Nl19
-->