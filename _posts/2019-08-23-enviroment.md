---
layout: post
title: "NLP 학습을 위한 기본적인 환경 구축 (Python 설치부터)"
tags: [setting]
comments: true
---
------개요------
 - Python 3.7 설치
 - Jupyter Lab 설치
 - Github 가입
 - Git Kraken 설치

# Python 3.7x Window 설치

많은 사람들이 (실제로 배움의 현장에서도) 파이썬을 시작하기 위해서 아나콘다부터 깔고 시작한다. 아나콘다는 **가상환경 변환이 쉽다**는 점과, **패키지 관리가 쉽다**는 점 때문에 많이 사용된다. 
  
하지만 실제로 NLP를 학습해보면 아나콘다에 없는 패키지를 **pip** *(파이썬 관련 패키지 설치 툴)*을 이용하여 깔아야 할 일이 많다. 즉, **어차피 아나콘다를 거치지 않는 것**이다. 사용하지 않는다면 용량도 큰 아나콘다를 굳이 유지할 필요가 없다.   
  
이에 파이썬만 깔아서 개발 환경을 설정하고자 한다.

## Python 설치
파이썬 홈페이지에서 [Downloads](https://www.python.org/downloads/windows/)로 들어가 [최신 Release](https://www.python.org/downloads/release/python-374/)가 무엇인지 확인한다. Python2와 Python3가 있는데, NLP를 하다보면 ML(머신러닝)을 돌려야하는 일이 종종 발생한다.  TensorFlow가 Python3.7 버전과 호환이 되는 지 [확인](https://tensorflow.blog/2019/02/03/tensorflow-1-13-0-support-python-3-7/) 한 후 Python3.7 을 설치했다.
"Windows x86-64 executable installer" Version을 [다운로드](https://www.python.org/ftp/python/3.7.4/python-3.7.4-amd64.exe)  받은 후 실행하면 된다.  
*(혹시 나와 같은 환경을 구축하려는 사람이 있다면 위의 '다운로드' 버튼만 누르면 된다)*

![enter image description here](https://lh3.googleusercontent.com/J8qs6nLvOQsBQxQyTgzeRB1PopP1nyKO287uBT50yAbbXWz-30nNHPmb6GpNO5YTAy0k9FybOA9H=s800 "install page")

설치 시에 이것저것 option이 많이 나온다.  
나는 아래와 같이 설치했다.

![enter image description here](https://lh3.googleusercontent.com/PgRDGhpKTUoRdSAAMEYqgP2ltNYiYyKpB1rVR52oNP_oyGidQU9O54OzExGn5mISvr9Z-kE6erfW "intall python1")
위에서 빨간색으로  체크박스(Add Python 3.7 to PATH)를 선택해주는 것이 나중에 정신 건강에 이롭다.  
그 다음 Customize installation을 선택해서 새로 경로를 지정해주면 나중에 삭제 시 깔끔하게 제거할 수 있다.
![enter image description here](https://lh3.googleusercontent.com/X6YwCISOqwbnwFMn5qLAeJUVou1xviJjdHYiBGRbKcz0aqgwK5EsZQY2PsPlF3OstW6LsgXRlSy7 "intall python2")
![enter image description here](https://lh3.googleusercontent.com/_GYsx1cCR-_HFYwAzjxJmnS79ZVw0bEBFimG0pk5IBuICy6mqQT9J0l9ADZL_8j-7EKp3ThG7Szx "intall python3")



## 가상환경 사용 (Python Venv)
가상환경 구축에는 [이 분의 블로그](https://yongbeomkim.github.io/python/python-settings/)를 많이 참고했다.  
먼저 cmd를 실행해여 다음과 같이 타이핑한다.
```
C:\> cd c:\Python
C:\Python> mkdir Venv
C:\Python> cd Venv
C:\Python\Venv> python -m venv NLP
```
위에서 한 행동은 파이썬 설치 시 만든 'Python' 폴더에 접근하고,
Venv 폴더를 cmd상에서 생성했으며,
그곳에 접근하여
python 의 명령어를 사용하여 'NLP'라는 이름의 가상환경을 만들어낸 것이다.
여기서 'NLP'는 Venv 내의 폴더로 만들어지기도 하고 가상환경의 이름이 되기도 한다. 이 작업이 완료되면 다음과 같은 작업을 통해 파이썬을 실행할 수 있다.
```
C:\Python\Venv> cd NLP\Scripts
C:\Python\Venv\NLP\Scripts>activate
```
그럼 다음과 같이 가상환경으로 진입할 수 있다.
```
(NLP) C:\Python\Venv\NLP\Scripts>
```

# jupyter lab 설치
설치 법에 대해 얘기하기 앞서, 내가 왜 jupyter lab을 선택했는지 기록핻
> jupyter Notebook이 아닌 jupyter lab을 사용하는 이유
## jupyter lab 설치
## jupyter lab 바로가기 만들기

# Github 가입
# GitKraken 설치



<!--stackedit_data:
eyJoaXN0b3J5IjpbMTczMzIxMjU1MCwtMTU3NDgyMjEzNCw0Nj
Y1MjMxNzcsLTE2Mzk2NjM1NDksLTEzMzgyOTM4MiwtMjQ0NzQ4
MjYsLTUxNDUyODcyOCwxNjMwMTk4MTM4LDE4MDIyMzMzODMsLT
IwNTA5Mzk2MDEsMTA0MjczMjM4Myw1NTkxMDM1MDksNzg0NTUx
MDY3LC0xMzg5ODIzMDk1LDk1NzU3NjExMSwtMjg2OTk4Mjc5LD
EyNTIxMDYzNSw3NDY2ODczOTgsMTQxMjM1OTk2MiwtMjc2MzU4
MDYxXX0=
-->