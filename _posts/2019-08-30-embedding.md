---
layout: post
title: "단어 임베딩 (Word Embedding)을 하는 4가지 방법"
tags: [study, nlp]
comments: true
---
단어 임베딩에는 여러가지 방법이 있다. 그 중에서 우리는 분산표현(Distributed Representation)의 4가지 모델에 대해 살펴보겠다. distributed representation은 continuous representation이라고도 한다.  
분산 표현은 **비슷한 위치에서 등장하는 단어들은 비슷한 의미를 가진다**라는 가정으로 출발한다. (앞서 설명했던 [밀집벡터](https://stellarway.github.io/embedding_basic/)의 가정과 동일하다)
Distributed Representation의 모델에는 크게 다음과 같이 4가지 모델이 있다.
* Word2Vec
* FastText
* GloVe
* LSA  

하나씩 살펴보자

## Word2Vec
Word2Vec는 의미가 보존되며, 심지어 [연산도 가능](word2vec.kr/search/)하다.  (물론 연산의 결과를 이해할 수 없는 값으로 리턴할 때도 있다) 
Word2Vec을 하는 방법에는 두가지 방법이 있다.**CBOW**(Continuous Bag of Words)와 **Skip-Gram** 방식이다.  
CBOW 방식은 주변에 있는 단어로 중간에 있는 단어를 예측하는 방식이고, Skip-Gram은 주변에 있는 단어로 중간 단어를 예측하는 방식이다.

## FastText
ㅇ넘뢴ㅇ러
FastText는 방법론적으로 Word2Vec과 비슷하다. (심지어 같은 분이 만드셨다)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgxMDYxNDIwOF19
-->