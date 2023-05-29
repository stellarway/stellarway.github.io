---
layout: default
---
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />

*This page is tailored for Korean users.  
If you're seeking information in English, please visit the '<a href="/">About</a>' page.*

## 🎲 Three Aspects to Focus
<hr class='section'>

> <span class="emphasis">Data</span>&emsp;다국어 자연어 데이터(한영중일) 처리 경험 보유.  
&emsp;&emsp;&emsp; 최대 1,200만여 쌍의 문장 쌍 처리 경험 있음.
> 
> <span class="emphasis">Model</span>&emsp;트랜스포머 기반의 NMT와 PLM 기반의 downstream task를 위한 LM 훈련 경험 다수.  
>&emsp;&emsp;&emsp;&emsp;여러 GPU로의 분산 훈련 경험 보유.
>
> <span class="emphasis">Recently</span>&emsp;번역문 품질 평가(QE) 관련 논문으로 우수논문상 수상 (<a href="asset/TwiQE.pdf">**paper**</a>)  
> <span class='subtitle'>→ 과기부와 NIA에서 개최한 ‘2022 AI 데이터 품질 개선 오픈랩 프로그램’ 챌린지에서 우수논문상 수상  
> → 한국정보과학회가 주관인 2022 한국소프트웨어종합학술대회(KSC2022)에 초청 받아 Poster 세션과 Oral 세션 참가  
> → 정보과학회 컴퓨팅의 실제 논문지(KTCP)에 초청 논문으로 제출, 1차 심사 중인 상태임  
> → "번역 품질 평가 장치 및 방법" 특허 출원 (출원번호: 1020220178652)</span>

<br>

## 👀 Summary
<hr class='section'>

For further details, please proceed to the below section<span class="subtitle">(w. 🌿 emoji)</span>.
<br>
<br>

Date|Project
----|-------
2023.01.11 - 2023.05.31 | 멀티모달 기반 웹툰 전용 번역기 연구 및 웹툰 병렬 데이터<br><span class="tag">구어체</span> <span class="tag">Multimodal</span> <span class="tag">NMT</span> <span class="tag">OCR</span>
2022.08.08 - 2022.12.21 | TwiQE: 한영/영한 번역 병렬 말뭉치 품질 예측 모델 구축 및 적용 (우수 논문 수상)<br><span class="tag">QE</span> <span class="tag">DA_score</span> <span class="tag">probing_task</span> <span class="tag">ML</span>
2022.04.27 - 2022.05.18 | 용어 추출기 개발<br><span class="tag">Terminology</span>
2022.02.10 - 2022.05.23 | 인공지능(AI) 학습용 데이터 구축 사업 ‘한영 구어체 및 기술과학 번역 말뭉치’구축 및 ‘방송 및 전문분야 다국어 번역 말뭉치’ 구축<br><span class="tag">NMT</span> <span class="tag">data</span>
2021.12.29 - 2022.01.17 | 텍스트 문장 비식별화 모델 개발<br><span class="tag">NER</span> <span class="tag">비식별화</span>
2021.07.13 - 2022.02.07 | NER 모델 개발 및 데이터 구축<br><span class="tag">NER</span>
2021.06.15 - 2021.09.27 | TTA 글로벌 사실표준화기구 정보 제공 시스템 구축 용역<br><span class="tag">DP</span> <span class="tag">NER</span>
2020.11.05 - 2021.04.23 | tagMT 연구<br><span class="tag">NMT</span>
2020.09.22 - 2020.12.31 | 인공지능(AI) 학습용 데이터 구축 사업 ‘영어번역말뭉치 AI 데이터’ 구축<br><span class="tag">NMT</span> <span class="tag">data</span>
2020.09.17 - 2021.04.24 | NER 리서치 및 데이터 구축<br><span class="tag">NER</span> <span class="tag">data</span>
2020.06.30 - 2020.08.26 | TD 관리 점검 및 구축<br><span class="tag">TD</span> <span class="tag">crawler</span> <span class="tag">data</span>
2020.06.03 - 2020.06.26 | 병렬 말뭉치 정제 및 검수 알고리즘 작성<br><span class="tag">corpus</span> <span class="tag">data</span>
2020.05.26 - 2020.06.05 | 병렬 말뭉치 크롤러 개발<br><span class="tag">corpus</span> <span class="tag">crawler</span> <span class="tag">data</span>

  

<br>
<br>

<!-- <hr class='section'> -->


## 🌿 Portfolio
<hr class='section'>
### 멀티모달 기반 웹툰 전용 번역기 연구 및 웹툰 병렬 데이터<a class="material-symbols-outlined outlink" target="_blank" href="https://news.mt.co.kr/mtview.php?no=2023030616452721288">call_made</a> 
<p class="project_date">2023.01.11 - 2023.05.31</p>
<span class="tag">구어체</span>
<span class="tag">Multimodal</span>
<span class="tag">NMT</span>
<span class="tag">OCR</span>

Skills | Python, PyTorch, Docker  
Summary |  맥락 정보가 필요한 짧은 구어체 위주의 웹툰 번역을 위한 멀티모달 기반 웹툰 전용 번역기 개발
Role | 연구 전반 리드, 데이터 구축 시 개발과 NLP가 필요한 부분을 기술 지원

* **Contributions** 
  - 태스크의 목적에 따라 연구 진행 단계 설계, 입력값과 출력값 정의, 데이터 명세, 데이터 전처리 알고리즘 작성, 데이터 구축 중간 단계 보조, 휴먼 에러 탐지 및 데이터 검수 알고리즘 작성, 모델 학습 과정 중 발생하는 이슈 파악 및 방향 제시, 모델 추론 코드 정리 및 AWS Lambda에 올리기 위한 형태로써 Docker 구성

* **Results & Accomplishments**
   - 해외적으로도 연구가 미비한 웹툰 영역에서의 멀티모달 모델 연구 진행
   - 휴먼 라벨링이 필요한 데이터 구축이 늦어지자 빠른 판단으로 수도 데이터(pseudo-data) 구축
   - 개발한 모델로 text-only의 구글 번역기보다 BLEU 점수가 높게 나옴.

* **Process**
1. 연구 설계 : 태스크의 성격을 정의하고 협의. 연구의 진행 단계 구성 및 모델의 인풋 아웃풋 정의
2. 데이터 파악 및 명세 작성 : 최종 산출물의 데이터 명세 및 메타 데이터의 범위 정의. 수량 파악
3. 리서치 진행 : 선행 연구 리서치 및 각 중간 단계에 적용 가능한 모델 선정
4. 데이터 구축을 위한 전처리 : 기계적 라벨링 진행
5. 데이터 검수 : 휴먼 에러를 감지하기 위해 각종 알고리즘을 설계해 에러 탐지
6. 모델 훈련 : 목적에 맞는 2~3개의 모델 탐색 및 성능 비교
7. 베이스라인과의 성능 비교
8. 배포: 추론 코드 정리 후 도커 환경으로 구성

---

### TwiQE: 한영/영한 번역 병렬 말뭉치 품질 예측 모델 구축 및 적용 (우수 논문 수상)<a class="material-symbols-outlined outlink" target="_blank" href="https://www.datanet.co.kr/news/articleView.html?idxno=179709">call_made</a> 
<p class="project_date">2022.08.08 - 2022.12.21</p>
<span class="tag">QE</span>
<span class="tag">DA_score</span>
<span class="tag">probing_task</span>
<span class="tag">ML</span>

Skills | Python, Huggingface, Scikit-learn
Summary | 적은 수의 데이터로도 번역 품질 평가가 가능한 실무적으로 경제적인 기계번역 평가 모델을 개발
Role | 연구 리드 및 논문 작성

* **Contributions** 
  - 선행 연구 조사, 연구 설계, DA 스코어링 가이드 초안 작성, 머신 러닝 학습, 논문 작성

* **Results & Accomplishments**
   - 한영/영한 DA score QE 데이터 3천 건 구축 (당시까지 전무했음)
   - 적은 수의 데이터로도 학습이 가능한 모델 개발
   - DA 점수 매기기 위한 가이드가 기존에는 다소 모호한 감이 있었으므로, 더 명확한 점수 가이드 제시
   - AI HUB에 공개되어 있는 병렬 말뭉치 중 총 4,185,507문장 쌍에 대해 분석 실시하여 평가, 전반적으로 품질이 좋지 않은 데이터셋을 찾아냄
   - 정보과학회 초청 논문으로 심사 대기 중이며, 관련 특허 출원
   - 사내 데이터 구축 프로젝트와 제품에 적극 활용 중


* **Process**
1. 아이디어 실험  
   \: 당시 실무(번역 병렬 말뭉치 의미적 검수)에 당장 필요한 모델이었으므로 자체 구축한 적은 수의 DA 데이터셋을 이용해 모델 실험 후 실제 데이터에 적용
2. 선행연구 조사  
   \: 번역문 품질 예측(Quality Estimation, 이하 QE), DA(Direct Assessment) score, 한국어가 포함된 QE task, PLM(Pretrained Language Model)의 문장 임베딩 능력 측정을 위한 probing task에 대한 선행 연구 조사
3. 연구 제안서 작성 및 제출  
  \: 과학기술정보통신부(이하 과기부)와 한국지능정보사회진흥원(이하 NIA)이 개최한 ‘2022 AI 데이터 품질 개선 오픈랩 프로그램’에 연구 제안서 제출  
  \: 연구 목표(500자 이내), 연구 방법(1,000자 이내), 방법론 근거(1,000자 이내), 연구 역량(1,000자 이내) 등 4가지 항목을 작성했음  
  \: 제출한 연구 제안서에 대해 ‘연구 목표의 적합성’, ‘연구 방법론의 명확성’, ‘연구 역량’ 등 세 가지 항목에 대해서 평가받았으며, 상위 20개 팀에 들어 본선 진출
1. 모델 실험 및 데이터 구축
2. 논문 작성 및 제출  
  \: 오픈랩 프로그램에서 공표한 논문 평가 기준은 아래와 같음  
  \- 해당 분야의 학술적 또는 산업적으로 중요한 주제를 다루고 있는가(10)  
  \- 해결하려는 문제와 해결 방안 및 결론을 명확히 기술하고 있는가(10)  
  \- 과거 관련 연구와 참고 문헌이 적절히 기술되어 있는가(20)  
  \- 신규성이나 기술적 우월성이 있는가(20)  
  \- 논문의 구성과 서술 방법이 적당하며 실험 또는 증명으로 적절히 검증되어 있는가(40)
1. 세션 발표  
  \: 2022년 12월 21일 한국정보과학회가 주관인 2022 한국소프트웨어종합학술대회(KSC2022)에 초청 받음  
  \: 상위 8개 팀만 참가 가능한 Oral 세션에 참가해서 발표, 최종적으로 상위 3개 팀에 선정됨
1. 학회에 초청 논문 제출 및 관련 특허 출원  
  \: 정보과학회 학회의 논문 규정에 맞게 편집 후 제출 (심사 대기 중)  
  \: "번역 품질 평가 장치 및 방법" 특허 출원 (출원번호: 10-2022-0178652)


---

### 용어 추출기 개발
<p class="project_date">2022.04.27 - 2022.05.18</p>
<span class="tag">Terminology</span>

Skills | Python, Regex, 형태소_분석기
Summary | ICT 분야 한국어 말뭉치에서 용어를 추출하는 알고리즘으로, 자체적으로 이슈를 감지하여 해결하기 위해 개발
Role | 주요 알고리즘 개발 및 적용

* **Contributions** 
  - 연구 기획 및 제안, 리서치, 주요 알고리즘 개발 및 적용

* **Results & Accomplishments**
  - 용어 추출기 개발
  - 데이터 구축 프로젝트에 활용됨
  
* **Process**
1. 이슈 감지 및 해결 방안 아이디에이션
2. 선행 연구 조사
3. 데이터 전처리
4. 알고리즘 개발
6. 테스트 및 보완

---

### 인공지능(AI) 학습용 데이터 구축 사업 ‘한영 구어체 및 기술과학 번역 말뭉치’구축 및 ‘방송 및 전문분야 다국어 번역 말뭉치’ 구축<a class="material-symbols-outlined outlink" target="_blank" href="https://www.aitimes.kr/news/articleView.html?idxno=22003">call_made</a> 
<p class="project_date">2022.02.10 - 2022.05.23</p>
<span class="tag">NMT</span>
<span class="tag">data</span>

Skills | Python, PyTorch, docker
Summary | 구축된 데이터가 신경망 기반 기계번역 학습 데이터로서 기능함을 보이기 위해, 제한된 데이터로 기계번역기 훈련 후 도커 형태로 모델 배포
Role | 데이터 유효성 검증을 위한 모델 훈련

* **Contributions** 
  - 데이터 유효성 검증을 위한 NMT 훈련(한영/영한/한일/일한/한중/중한), 모델 추론 도커 환경 구성, 실행 매뉴얼 작성

* **Results & Accomplishments**
  - 총 6개 언어쌍(한영/영한/한일/일한/한중/중한) 각각으로 단일 방향의 NMT 훈련 후 배포
  - 총 4개의 데이터 셋의 데이터를 다뤘으며, 그 목록은 아래와 같음
    - 일상생활 및 구어체 번역 병렬 말뭉치 데이터
    - 기술과학 분야 한-영 번역 병렬 말뭉치 데이터 
    - 식품 전문분야 영-한,중-한 번역 말뭉치
    - 방송 콘텐츠 한-중, 한-일 번역 병렬 말뭉치 데이터
  - 각 언어쌍 별 데이터 수량은 아래와 같음
    - 한-영 총 300만 가량
    - 영-한 총 300만 가량
    - 한-일 총 75만 가량
    - 일-한 총 45만 가량
    - 한-중 총 75만 가량
    - 중-한 총 195만 가량
  - 데이터 유효성이 확인되었으며, 현재 4개의 데이터셋은 AI HUB에 공개되었음

* **Process**
1. 데이터 검수 및 전처리
2. 모델 피드 형식으로 데이터 변환
3. NMT 훈련 및 결과 확인
4. NMT 추론 코드 도커 환경 구성
5. 도커에서의 NMT 추론 실행 매뉴얼 작성

---

### 텍스트 문장 비식별화 모델 개발<a class="material-symbols-outlined outlink" target="_blank" href="https://www.epnc.co.kr/news/articleView.html?idxno=220996">call_made</a> 
<p class="project_date">2021.12.29 - 2022.01.17</p>
<span class="tag">NER</span>
<span class="tag">비식별화</span>

Skills | Python, PyTorch, Regex
Summary | 비식별화 데이터셋 구축 후 비식별화 모델 개발, API로 서비스되는 모델로 탑재
Role | 모델 훈련

* **Contributions** 
  -  비식별화 대상 항목에 해당하는 엔터티에 대해 기계적 데이터셋 구성, 비식별화 대상 항목에 해당하는 엔터티에 대해 모델 훈련
  
* **Process**
1. 데이터 수집
2. 비식별화 수도 라벨링 데이터셋 구성
3. 데이터 전처리
4. 모델 학습
5. 실무 적용

---

### NER 모델 개발 및 데이터 구축
<p class="project_date">2021.07.13 - 2022.02.07</p>
<span class="tag">NER</span>

Skills | Python, PyTorch, Regex
Summary | NER 데이터 자체 구축 및 NER 모델 훈련
Role | 데이터 검수와 후처리, 모델 훈련

* **Contributions** 
  - 데이터 검수, 기계적으로 구축 오류 교정, 모델 훈련, 리서치 보고서 작성
  
* **Results & Accomplishments**
  - 총 168,101 문장 분량에 해당하는 NER 데이터 자체 구축 
  - API에 탑재되는 NER 모델 훈련

* **Process**
2. NER 데이터 검수 및 구축 오류 기계적 교정
3. 기존 NER 데이터셋 조사 및 전처리  
   \: 카테고리 일치시킴  
   \: 데이터 기계적 검수  
   \: 모델 피드 형식으로 데이터 변환  
4. NER 모델 훈련
5. 추론 코드 분리 및 API로 서비스



---

### TTA 글로벌 사실표준화기구 정보 제공 시스템 구축 용역
<p class="project_date">2021.06.15 - 2021.09.27</p>
<span class="tag">DP</span>
<span class="tag">NER</span>

Skills | Python, tensorflow, Regex, 형태소 분석기
Summary | 한국어 구어체 표현의 특성 상 일어나는 기계 번역 결과의 왜곡을 교정하기 위한 연구 수행
Role | 인공지능 기계번역기 모델링 연구원


* **Contributions** 
  - 아이디에이션, 데이터 기계적 구축, 선행연구 조사, 논문 구현, 모델 훈련, 데이터 구축 방향 제안

* **Process**
1. 문제 정의 및 해결 방안 아이디에이션
2. 문맥 상황에서의 과제 해결 방안 제안 및 알고리즘 작성
3. 2단계에서의 방법으로는 많은 예외 상황이 발생해, 딥러닝 기반 선행 연구 조사
4. 데이터셋 자동 구축 방법 제안
5. 논문 구현
6. 모델 훈련

---

### tagMT 연구
<p class="project_date">2020.11.05 - 2021.04.23</p>
<span class="tag">NMT</span>

Skills | Python, Pytorch, Regex
Summary | 문서 번역 시 일어나는 기계 번역 결과의 왜곡을 근원적으로 해결하기 위한 연구 수행
Role | 인공지능 기계번역기 모델링 연구원

* **Contributions** 
  - 요구 사항 정의, 데이터셋 구축 기술 지원, 평가 코드 작성, 모델링 연구 수행

---

### 인공지능(AI) 학습용 데이터 구축 사업 ‘영어번역말뭉치 AI 데이터’ 구축
<p class="project_date">2020.09.22 - 2020.12.31</p>
<span class="tag">NMT</span>
<span class="tag">data</span>

Skills | Python, Pytorch, Regex
Summary | pdf 파일이나 docx 파일에서 추출한 텍스트 정제
Role | 원천 데이터 정제

---

### NER 리서치 및 데이터 구축<a class="material-symbols-outlined outlink" target="_blank" href="https://www.letr.ai/blog/tech-20210723">call_made</a> 
<p class="project_date">2020.09.17 - 2021.04.24</p>
<span class="tag">NER</span>
<span class="tag">data</span>

Skills | Python, PyTorch, Regex
Summary | 당시 NER 관련한 선행 연구와 국제적, 국내적 데이터와 모델 상황을 조사했으며, 목표 성능을 제안하고 NER 데이터 구축 시 개발과 NLP가 필요한 부분을 기술 지원함
Role | 리서치(2020.09.17 - 2020.09.24), 모델 성능 비교(2020.10.28 - 2020.11.03) 및 데이터 구축을 위한 전처리 (2020.12.16 - 2021.04.24)

* **Contributions** 
  - NER 기공개된 데이터셋 리서치, 모델 리서치, 모델 성능 비교
  
* **Results & Accomplishments**
  - 당시 NER 데이터셋과 모델을 총망라한 수차례의 보고서를 발간
  - 당시 발간된 보고서 중 일부 내용 기반으로 작성한 블로그 글은 현재까지도 ’NER’ 검색 시 최상단에 노출된
  - 데이터 전처리를 통해 NER 데이터를 구축할 수 있도록 기술 지원

* **Process**
1. 기존 한국어 NER 데이터 셋 조사  
2. 한국어가 학습된 NER 모델 조사 
3. 기존 영어 NER 모델 성능 비교  
4. 기존 한국어 NER 모델(multi-language model) 성능 비교
6. 보고서 발간  
  \: 개론과 현황, 나아가야 할 방향에 대해 총 20쪽 가량의 최종 리서치 보고서를 작성했으며, 보고서 작성 시 들어간 항목은 다음과 같음  
    **\- AS-IS**
  (1)	NER의 정의
  (2)	NER이 기계 번역에 필요한 이유와 배경
  (3)	NER 성능 평가 지표
  (4)	NER의 태깅 시스템과 라벨
  (5)	NER에 대한 다양한 접근법과 딥러닝 기반의 NER
  (6)	NER의 모델 구조
  (7)	현재 시중에 나와있는 NER 관련 라이브러리와 성능 평가
  (8)	현존 영어 NER 데이터 셋 (대표적인 네 가지)
  (9)	현존 한국어 NER 데이터 셋  
    **\- TO-BE**
  (1)	NER 모델 개발 방향
  (2)	한국어 NER 데이터 셋 구성의 필요성
  (3)	원문 데이터 확보 방안
  (4)	데이터 구성의 절차
  (5)	데이터의 구체적인 형태
  (6)	데이터 셋의 개수 목표 산출
  (7)	한국어 NER 모델의 최종 목표
6. NER 데이터 구축을 위한 선라벨링

---

### TD 관리 점검 및 구축
<p class="project_date">2020.06.30 - 2020.08.26</p>
<span class="tag">TD</span>
<span class="tag">crawler</span>
<span class="tag">data</span>

Skills | Python, Regex
Summary | 자체 보유하고 있는 TD에 대해 현황 파악 후 고도화
Role | 연구원

* **Contributions** 
  - TD 현황 파악, 분류 체계 정립, 오타 점검 크롤러 개발, 용어집 리스트 조사 및 크롤링

---

### 병렬 말뭉치 정제 및 검수 알고리즘 작성
<p class="project_date">2020.06.03 - 2020.06.26</p>
<span class="tag">corpus</span>
<span class="tag">data</span>

Skills | Python, Regex
Summary | 병렬 말뭉치를 정제하고 검수할 수 있는 알고리즘 작성
Role | 연구원

* **Contributions** 
  - 병렬 말뭉치 에러 케이스 정의, 검수 알고리즘 작성, 정제 알고리즘 작성

---

### 병렬 말뭉치 크롤러 개발
<p class="project_date">2020.05.26 - 2020.06.05</p>
<span class="tag">corpus</span>
<span class="tag">crawler</span>
<span class="tag">data</span>

Skills | Python, Regex
Summary | 다국어 웹페이지에서의 병렬 말뭉치 크롤러 개발
Role | 연구원

* **Contributions** 
  - 간단한 변수 변경으로 세 개의 웹사이트 크롤링이 가능한 코드 개발
  - 다국어 페이지의 원하는 depth까지 하이퍼 링크를 타고 들어가면서 언어 쌍을 맞추는 크롤러 개발


<br>
<br>
<br>

<!-- ## References
---
* Foo Bar: Head of Department, Placeholder Names, Lorem
* John Doe: Associate Professor, Department of Computer Science, Ipsum -->
