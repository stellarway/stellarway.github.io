---
layout: post
title: "텍스트 전처리 용어 정리"
tags: [study, preprocessing]
comments: true
---
기본적인 텍스트 마이닝 절차는 다음과 같다.
> 1. 데이터 수집 단계  
	> (수집/정제)
> 2. 텍스트 전처리 단계
	> ( 토큰화/ 품사 부착/ 원형 복원/ 불용어 처리)
>3. 텍스트 분석 단계 
	>(주제어 찾기/ 문서 요약/ 문서 분류/ 감성 분석)
>4. 시각화 단계

텍스트 마이닝을 위한 기본 단계, 즉 데이터 수집 단계는 앞서 [BeautifulSoup](https://stellarway.github.io/beautifulsoup/)과 [Selenium](https://stellarway.github.io/selenium/), scrapy를 통해 정리해보았다.

### 토큰화(Tokenization)
언어를 배우는 아기를 생각해보면, 먼저 "맘마", "엄마" 등의 단어부터 학습한다. 기계도 똑같다. 단어를 학습시켜줘야한다. 따라서 단어 단위로 잘게 쪼개는 과정이 먼저 필요하다. 이를 토큰화라고 한다. 문장으로 쪼개고(Sentence Tokenization) 이것을 다시 단어로 쪼갠다(Word Tokenization)

### 품사 부착(Part-of-Speech Tagging)
쪼개진 단어에는 품사가 따라 붙는데, 이것은 분석에 불필요한 정보인 조사나 접속사 등을 제거하거나, 혹은 필요한 품사들만골라보기 위해 사용된다.

### 개체명 인식(NER : Named Entity Recognition)
개체명 인식은 분리된 토큰이 사람인지, 조직인지, 지역인지, 숫자인지 등, 개체 유형을 식별해주는 것을 말한다.

### 어간 추출과 표제어 추출(Stemming & Lemmatization)
**Stemming**은 어간 추출로,  일정한 규칙에 기반하여 어간을 추출하는 방식이다. 'run'과 'running'이 사실상 같은 의미를 뜻하고 있으니 이 둘을 같은 단어로 치기 위하여 현재진행형을 없애주는 것이다. 하지만 'studies'와 같은 경우 규칙에 기반하여 복수형 표현인 '-es'를 없애주면 사실상 무슨 단어인 지 잘 구분이 되지 않는다. 그래서 나온 것이 **Lemmatization**이다.  
**Lemmatization**은 표제어 추출로, 사전 기반으로 토큰을 표준화하는 방식이다.

### 불용어 처리(Stopwords)
아까 품사 부착(PoS Tagging)에서도 잠깐 언급했듯이, 분석에 불필요 한 단어나 품사를 걸러주는 과정이다.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExNzM1NDE3Nl19
-->