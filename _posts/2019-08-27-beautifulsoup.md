---
layout: post
title: "크롤링(crawling)의 도구 1 - BeautifulSoup"
tags: [scraping, crawling, study, beautifulsoup]
comments: true
---
크롤링은 데이터를 모으기 위한 첫번째 방법이다. 가장 필요한만큼 많은 방법이 존재한다.
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
위와 같이 파라미터를 별도 지정해줄 수 있다. (여기서 'sm=tab_jum' 는 빠졌는데,  리퀘스트 보낼 때는 없어도 상관 없는 요소이다) 여기서 `resp.url`을 입력하면 해당 url이, `resp.status_code`를 입력하면 `200`이 뜬다. 200은 url이 정상적인 신호를 나에게 주고 있다는 뜻이다. `resp.ok`도 있는데, 정상적인 접속일 경우 `True`가, 에러가  있을 경우 `False`가 뜬다.

위에서 url을 쭉 적는 대신 파라미터를 지정해 준 이유는, 후에 keword를 자유롭게 바꾸기 위함이다.

검색 페이지에서 내가 크롤링해 올 정보를 정한다. 이번 크롤링으로 다음과 같은 정보를 가져오고자 한다.
![enter image description here](https://lh3.googleusercontent.com/B56CfAL1HpKj3EClyImiyHd_-S0afnp8D_eUx6mTu9_ZZCbUMy6kAXXFioXdVWR3TyMYBLI8Xz_p=s1000)
전체 건수와 각각의 제목/ 뉴스사/ 게시 시간이 그 대상이다.
웹페이지 상에서 `F12` 키를 누른 후 `Ctrl+Shift+C`를 누르면 내가 궁금한 부분이 코드로 어떻게 이루어졌는지 볼 수 있다. 일단 건수부터 가져와 보겠다.

![enter image description here](https://lh3.googleusercontent.com/LTi8AEMYmv0uwDY-w_C4XCyZE3JShvblb76Z_kuG7VmP_sqIGqhGifsZviJIU3tK3Tl3BPOmYbvh=s1000)
화살표에 마우스를 가져다 대면 아래에 스크립트 중 해당 부분이 하이라이팅 되며 나타난다.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTIyMjIwODkyXX0=
-->