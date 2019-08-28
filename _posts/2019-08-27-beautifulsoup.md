---
layout: post
title: "크롤링(crawling)의 도구 1 - BeautifulSoup"
tags: [study, crawling]
comments: true
---
크롤링은 데이터를 모으기 위한 첫번째 방법이다. 가장 필요한만큼 많은 방법이 존재한다.  
파이썬에서 크롤링을 하는 방법은 크게 세가지가 있다. 오늘은 가장 먼저 배우게 되는 BeautifulSoup에 대해 정리해보겠다.

## BeautifulSoup 크롤링 기본
필요한 모듈은 다음과 같다.
```py
import requests
from bs4 import BeautifulSoup
```
네이버 뉴스를 한번 크롤링 해보자  
검색 keyword를 NLP로 해보겠다.

![enter image description here](https://lh3.googleusercontent.com/21fDklf-ttwBdt4h14RtCTLNpyH51dVQvICbfKwW5XVa_kqCHkpr-4AVo2wFLkBqF5rOJV2tb_hF=s700)

검색어를 입력하고 '뉴스'탭에 들어가면 위와 같은 주소가 나온다.   
url 주소를 잘 뜯어보면 물음표 부호 뒤에 이것저것 써있다. 앞으로 저 물음표를 기준으로 본다.  
물음표 기준으로 물음표 앞은 도메인, 뒤는 파라미터이다.
```py
url = 'https://search.naver.com/search.naver'
keyword = 'nlp'
params = {'where':'news', 'query': keyword}
resp = requests.get(url, params = params)
```
위와 같이 파라미터를 별도 지정해줄 수 있다. (여기서 'sm=tab_jum' 는 빠졌는데,  리퀘스트 보낼 때는 없어도 상관 없는 요소이다) 여기서 `resp.url`을 입력하면 해당 url이, `resp.status_code`를 입력하면 `200`이 뜬다. 200은 url이 정상적인 신호를 나에게 주고 있다는 뜻이다. `resp.ok`도 있는데, 정상적인 접속일 경우 `True`가, 에러가  있을 경우 `False`가 뜬다.  
  
위에서 url을 쭉 적는 대신 파라미터를 지정해 준 이유는, 후에 keword를 자유롭게 바꾸기 위함이다.  
  
검색 페이지에서 내가 크롤링해 올 정보를 정한다. 이번 크롤링으로 다음과 같은 정보를 가져오고자 한다.
![enter image description here](https://lh3.googleusercontent.com/B56CfAL1HpKj3EClyImiyHd_-S0afnp8D_eUx6mTu9_ZZCbUMy6kAXXFioXdVWR3TyMYBLI8Xz_p=s1000)
전체 건수와 각각의 제목/ 제목에 걸린 링크 주소가 그 대상이다.  
웹페이지 상에서 `F12` 키를 누른 후 `Ctrl+Shift+C`를 누르면 내가 궁금한 부분이 코드로 어떻게 이루어졌는지 볼 수 있다. 일단 건수부터 가져와 보겠다.  

![enter image description here](https://lh3.googleusercontent.com/LTi8AEMYmv0uwDY-w_C4XCyZE3JShvblb76Z_kuG7VmP_sqIGqhGifsZviJIU3tK3Tl3BPOmYbvh=s1000)
원하는 정보에 마우스를 가져다 대면 아래에 스크립트 중 해당 부분이 하이라이팅 되며 나타난다.  
저 정보의 위치를 특정하기 위해서는 태그의 이름과 클래스의 이름이 필요하다.   
김땡땡이라는 이름 하나만으로는 사람을 특정하기 어렵지만 서울시 서초구 무슨동에 사는 김땡땡씨라고 하면 특정하여 찾아내기가 더 쉬운 것과 마찬가지다.  

`<div>`나 `<span>`등이 태그 이름이고 주황빛을 띤 `class` 이하가 클래스 네임이다.  물론 `<span>` 태그를 입력하여 한방에 찾아내면 좋겠지만 이건  1602호에 사는 김씨 찾는 격이다. 따라서 우리는 '서울시 서초구'부터 접근한다. 즉, 그 바로 위인 `<div class-"title desc all_my">`부터 접근하는 것이다.  
저걸 찾기 위해 일단 전체 정보를 담은 `soup`를 만든다.  
```py
soup = BeautifulSoup(resp.content, 'html.parser') # 'html.parser'는 생략 가능
```
(`resp.content`만 따로 떼어서 보면, 리퀘스트 받는 모든 정보를 바이너리 형태로 저장하는 듯 하다)  
이제 내가 원하는 정보를 찾을 준비가 끝났다.  
```py
soup.find('div', class_='title_desc all_my')
```
여기서 class에 밑바를 붙이는 이유는 기존 파이썬 내장 변수인 class와 구분하기 위함이다. 위의 코드까지 실행하면 다음과 같이 출력된다.  
> <div class="title_desc all_my"><span>1-10 / 3,780건</span></div>

내가 원하는 값은 '3780'이라는 숫자이다. 
```py
num = soup.find('div', class_='title_desc all_my').text.split(' ')[-1].replace('건','').replace(',','')
int(num)
```
태그에서 text형을 찾아내고 공백(' ')을 기준으로 쪼개어 마지막 요소인 '3,780건'을 가저온다. 여기서 숫자로 바꾸는데 거슬리는 '건'이라는 한글과 쉼표(,)를 없애주고 마지막으로 `int`형으로 형변환 시켜준다.  
> 여기서 잠깐! 위에서는 없애줄 문자가 2건밖에 되지 않았지만 변환해야 할 문자수가 늘어나면 [translate 메서드](https://docs.python.org/3/library/stdtypes.html#str.translate)를 사용해보자! translate안에는 딕셔너리 형태의 인자가 들어간다. [이 분](https://godoftyping.wordpress.com/2015/04/05/%EC%97%AC%EB%9F%AC-%EA%B0%9C%EC%9D%98-%EB%AC%B8%EC%9E%90character-%EB%B3%80%ED%99%98%ED%95%98%EA%B8%B0/comment-page-1/)의 블로그를 참고해 보자

translate 메서드를 이용하여 쓸모없는 문자열을 없애주는 코드는 다음과 같다
```py
num = soup.find('div', class_='title_desc all_my').text.split(' ')[-1]
num = num.translate({ord('건'):'', ord(','):''})
int(num)
```
(하지만 `%timeit`코드를 넣어 시간을 측정해본 결과 2건 정도의 간단한 텍스트 변환에는 replace가 더 빨랐다)  
  
이제 비슷한 원리를 이용해 각각의 제목/ 제목에 걸린 링크 주소를 가져와 보자
```py
ul_list=soup.find('ul', class_='type01').findAll('dl')

for ul in ul_list:
    title=ul.find('dt').find('a')['title']
    link=ul.find('dt').find('a')['href']
    news_dict={
        'title':title,
        'link':link
    }
    news_list.append(news_dict)
```
이를 실행하면 각각의 제목과 링크를 담은 딕셔너리의 리스트 형태로 반환된다.

## Select 함수 (CSS selectors)
### CSS selectors 적용

BeautifulSoup에서 select 함수는 find보다 표기법이 간단하여 종종 쓴다.  
select 함수를 이용하여 총 몇건의 데이터가 있는지를 가져오는 코드를 작성하면 다음과 같다.  
```py
num = soup.select('div.title_desc')[0].text
```
select를 사용할 때 주의할 점은 다음과 같다.
> 1. 띄어쓰기 주의
> 2. 리스트 형태로 반환된다.

가끔 클래스 명에 띄어쓰기가 있던데, select에서 띄어쓰기는 하위 태그를 가져오라는 뜻으로 인식된다.  
또한 리스트 형태로 반환되기 때문에 이것을 풀어줘야 한다는 점을 명심해야 한다.  
하지만 이 **리스트 형태로 반환**되는 성질 때문에 더 쉽게 풀리는 코드도 있다. 위에서 제목 가져오는 코드는 select함수로 다음과 같다.

```py
for tag in soup.select('ul.type01 dt a'):
	title = tag['title'] # 혹은 title = tag.get('title')로 실행해도 된다.
```
### CSS selectors 문법
CSS selectors 문법을 정리하면 다음과 같다.  
크롤링 하다보면 자주 나오는 'div' 태그와 그 하위 태그인 'a' 태그가 있다고 생각해보자

|속성| 표기 | 예시| 뜻
|--|--|--|--
|바로 밑 태그| > | 'div > a'| div 태그 바로 아래에 있는 a 태그
| 하위 태그 | (공백) | 'div a'| div 태그 아래에 있는 a 태그
| id | # | 'div#sampleID'| id가 sampleID인 div 태그
| class | . | 'div.sampleClass'| class명이 sampleClass인 div 태그

이상으로 BeautifulSoup의 기본과 select함수에 대해 정리해보았다.  
다음에는 selenium을 사용하는 방법에 대해 정리해보겠다.

## Image 파일 저장하기
크롤링을 하다보면 이미지 파일을 긁어올 일이 생긴다. (물론 저작권에 아주 많이 유의를 해야한다)  
여기서는 구체적인 예시보다는 하는 방법에 대해 적어두겠다.  
먼저, 가져오고자 하는 이미지가 저장된 url을 검사를 통해 알아낸다.
```py
img_url = "저장하려는 이미지의 url"
resp = requests.get(img_url)
```
대량의 이미지를 긁어오다보면 filename이 겹치지 말아야 한다. 여기서는 이미지 url을 사용하여 filename을 정한다.
```py
path = '원하는 경로'
filename = path + img_url.split('/')[-1]
with open(filename, 'wb')as f:
	f.write(resp.content)
```
이렇게 하면 내가 지정한 폴더 경로에 이미지가 저장된다. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5ODAwMDI3ODFdfQ==
-->