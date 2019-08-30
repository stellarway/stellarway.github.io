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

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI2MTE2OTE3MF19
-->