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

![enter image description here](https://lh3.googleusercontent.com/J8qs6nLvOQsBQxQyTgzeRB1PopP1nyKO287uBT50yAbbXWz-30nNHPmb6GpNO5YTAy0k9FybOA9H=s800 "install page"){: .center-image}

설치 시에 이것저것 option이 많이 나온다.  
나는 아래와 같이 설치했다.

![enter image description here](https://lh3.googleusercontent.com/PgRDGhpKTUoRdSAAMEYqgP2ltNYiYyKpB1rVR52oNP_oyGidQU9O54OzExGn5mISvr9Z-kE6erfW "intall python1"){: .center-image}
위에서 빨간색으로  체크박스(Add Python 3.7 to PATH)를 선택해주는 것이 나중에 정신 건강에 이롭다.  
  
그 다음 Customize installation을 선택해서 아래 사진과 같이 새로 경로를 지정해주면 나중에 삭제 시 깔끔하게 제거할 수 있다.

![enter image description here](https://lh3.googleusercontent.com/_GYsx1cCR-_HFYwAzjxJmnS79ZVw0bEBFimG0pk5IBuICy6mqQT9J0l9ADZL_8j-7EKp3ThG7Szx "intall python3")
{: .center-image}

## 가상환경 사용 (Python Venv)
가상환경 구축에는 [이 분의 블로그](https://yongbeomkim.github.io/python/python-settings/)를 많이 참고했다.  
먼저 cmd를 실행해여 다음과 같이 타이핑한다.
```
C:\> cd c:\Python 						# 파이썬 설치 시 만든 'Python' 폴더에 접근
C:\Python> mkdir Venv 					# Venv 폴더를 cmd상에서 생성
C:\Python> cd Venv 
C:\Python\Venv> python -m venv NLP	 	# 'NLP'라는 이름의 가상환경을 만들어냄
```
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
## jupyter lab의 설치
설치 법에 대해 얘기하기 앞서, 내가 왜 jupyter lab을 선택했는지 기록해두려 한다.
jupyter lab은 jupyter notebook을 기반으로 만들어진 것이어서 기본적인 jupyter notebook의 특성을 따른다.
많은 사람들은 jupyter notebook을 선택함에 비해 내가 jupyter lab을 기본 환경으로 설정하려는 이유는 다음과 같은 장점이 있기 때문이다.

> 1. 파일 브라우징이 간편하다 (폴더트리가 바로 왼쪽에 떠있어서 여러 코드를 참고하기에 간편하다)
> 2. 마지막에 열었던 파일이 바로 실행된다.

  jupyter lab을 설치하는 것은 간단하다. 설치하고자 하는 가상환경으로 들어가 `pip install jupyterlab`을 타이핑해주면 된다.
```
(NLP) C:\Python\Venv\NLP\Scripts> pip install jupyterlab
```

## jupyter lab 바로가기 만들기
한편, 아나콘다 없이 바로 jupyter lab을 설치하면 바로 접근하기가 불편한다.  
간단한 작업으로 jupyter lab을 바로 실행할 수 있다.  
먼저 로컬에서 다음과 같은 폴더 경로로 접근한다.
> C:\Python\Venv\NLP\Scripts

그럼 'activate' 파일을 볼 수 있을 것이다. 
![enter image description here](https://lh3.googleusercontent.com/yAKxaVOMRMZiEKJb886RoUAlFjIrGf6ePq4fvbr-3vrRgIhJ4mX4N2HW2wS-gp89tFS1bTu5ahxt)
{: .center-image}
그것을 메모장으로 열어 맨 아랫쪽에 다음 두 줄을 추가해준다.
```
cd C:\Python\Ground
jupyter lab
```
위의 코드에서 Ground는앞으로 jupyter lab을 통해 작업하는 파이썬 파일들이 저장될 곳이다.  
~~(여담이지만 학원 등에서 배우며 만들었던 파일을 Playground, 개인적으로 따로 작업한 파일은 HomeGround에 저장을 해왔기 때문에 폴더 이름을 'Ground'로 정했다)~~
개인마다 마음에 드는 이름을 'Ground' 부분에 넣으면 된다.

이제 바로가기를 만들어보자  
아까 수정했던 activate 파일에 오른쪽 버튼을 누르면 '바로가기 만들기' 버튼이 있다. 이것을 클릭하여 바로가기를 생성한 뒤 내가 원하는 이름을 붙여주자. (나는 'NLP lab'이라고 이름을 붙였다)  

바로 이용할 수도 있지만, 임시파일처럼 생긴 아이콘을 참을 수 없어 아이콘을 변경해주고 한다.  
만들어 놓은 바로가기에서 속성을 눌러 들어가면 아이콘 변경을 할 수 있다.
![enter image description here](https://lh3.googleusercontent.com/gIPhuyCTs8FQ7B6_pluP8MCg3xJHwOeWm26j19SxRpVtHqQ1NP_Lr4kU6WZhTz_XxAGJ49chVQHu)
{: .center-image}
아이콘 변경을 위해서는 아이콘이 필요하다.  
구글링을 통해 원하는 이미지를 다운받는다. 나는 jupyter의 로고를 다운받았다.   
아이콘으로 넣기 위해서는 [이미지 파일을 ico 형식으로 변환](https://convertio.co/kr/png-ico/)해줘야 한다.
ico 형식의 파일을 찾아 넣으면 예쁘게 잘 들어간 것을 확인할 수 있다.  
  
이렇게 커스터마이징한 바로가기를 C드라이브의 사용자 폴더 안에 넣어주면  jupyter lab으로 바로 접근이 가능하다.  
![enter image description here](https://lh3.googleusercontent.com/3lrHyp3t5xLIFdw5dM8AmMQoiSPDMhYRruzyuxj_t9nZMWkRpVARsSD49lXXDr6KidtwsEdp_mb7)
{: .center-image}

이제 윈도우 자체의 검색창에서 지정한 앱 이름을 타이핑하면 NLP 가상환경 내의 jupyter lab이 시행된다.


# Github 가입
# GitKraken 설치
# Stackedit 사용


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc5MDg0MzUzOSwxNzUwODA3MjczLDIwMD
E5NzgxODQsLTE1Mjc5OTI3OTUsMzk5NjMwMTI1LDYzMTgwNDQ2
OCwtNTI2MDY1MjY4LC0xMDA3MzEwMjY1LC0xNTc0ODIyMTM0LD
Q2NjUyMzE3NywtMTYzOTY2MzU0OSwtMTMzODI5MzgyLC0yNDQ3
NDgyNiwtNTE0NTI4NzI4LDE2MzAxOTgxMzgsMTgwMjIzMzM4My
wtMjA1MDkzOTYwMSwxMDQyNzMyMzgzLDU1OTEwMzUwOSw3ODQ1
NTEwNjddfQ==
-->