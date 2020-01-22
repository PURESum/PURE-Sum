# 자연어 처리 기초 #1
2020.01.22
## 임베딩 (embedding)
언어를 숫자로 바꾸고 (vectorization) 이 벡터를 계산하여 사람이 이해하는 것에 가까운 의미로 해석하는 작업

### 임베딩 역할
1. 단어와 문장 사이 관련도 계산
- 코사인 유사도 (similarity)
- Word2Vec
- t-SNE (차원 축소 시각화)

2. 의미 또는 문법 정보 함축
- 단어 유추 평가 (word analogy test)
단어 의미의 차이가 임베딩 벡터와 관련 있을 때

3. 전이 학습 (transfer learning)
embedding을 또 다른 deep learning model의 입력으로 활용하는 것
0부터 시작하지 않는다

- FastText
분류 정확도 증가
학습 손실 감소

### 임베딩 기법의 역사와 종류
1. 통계 기반에서 neural network 기반으로
2. 단어 수준에서 문장 수준으로
BERT(Bidirectional Encoder Representation forn Transformer)
GPT(Generative PreTraining)

3. rule -> end-to-end -> pre-train/fine tuning
	1. Rule-base: 사람이 직접 feature (규칙, 모델의 입력)를 추출
	2. End-to-End: 사람의 개입 없이 입출력 관계를 모델이 유추
	3. Pre-train: 대규모 말뭉치 사용
	4. Fine tuning: dataset에 적합하도록 모델 전체를 업데이트

### Downstream task와 upstream task
- Downstream
1. 품사 판별 (Part of Sentences(POS) tagging)
2. 개체명 인식 (Named Entity Recognition(NRE)): 명사 구 (noun phrase)
3. 의미역 분석 (Semantic Role Labeling): 피행위 주역
- Upstream task: 임베딩 작업

### 임베딩 종류
1. 행렬 분해 (factorization)
GloVe, Swivel
행렬을 2개 이상의 작은 행렬로 분할하고 분할된 행렬을 임베딩에 사용
2. 예측 기반
Word2Vec, FastText
3. 주제 (topic) 기반



# 자연어 처리 기초 #2
## 벡터가 어떻게 의미를 갖게 되는가?
### 1. 백오브워즈 과정 (Bag of Words: BoW)
#### 어떤 단어가 (많이) 쓰였는가
- **tf-idf** (Term Frequency - Inverse Document Frequency)
- Deep Averaging N/W
단어가 나타난 순서를 고려하지 않는다.

### 2. (통계 기반) 언어 모델
#### 단어가 어떤 순서로 쓰였는가
단어 sequence 에 확률을 부여한다.
N개 단어가 있을 때, N개 단어가 동시에 나타날 확률을 계산한다.
이웃해서 자주 나타난 던어 쌍일수록 확률이 높다.
Ex)
두시 삼십이분 -> 0.51
이시 서른두분 -> 0.08

- n-gram model
[난폭, 운전], [눈, 뜨다] -> 2-gram (bigram)
[누명, 을, 쓰다] -> trigram
[바람, 잘 , 날 ,없다] -> 4-gram

- 최대 우도 추정 (maximum likelihood estimation)
	- Markov chain
	직전 n-1개 단어 발생 확률로 전체 단어 sequence 발생 확률을 근사
	직전 1개 단어만으로 전체 단어 sequence 발생 확률을 추정

바이그램 모델 형태로 쪼개서 계산
**조건부 확률 (종속 확률)** 

#### N-gram 모델의 약점: 중간에 자주 사용하지 않는 단어가 있을 경우 확률이 0이 된다.
1. Backoff: n-gram 대신 작은 gram으로 근사
빈도가 0인 단어가 포함될 적용

2. Smoothing


### 3. 분포 가정
#### 어떤 단어가 같이 쓰였는가
분포: 특정 범위 내에 동시에 나타나는 이웃 단어 또는 문맥의 집합
단어 쌍이 문맥에서 자주 등장한다면 그 의미도 유사할 것이라고 가정

- 전별 상호 정보량 PMI (Pointwise Mutual Information)
두 확률변수 사이의 상관성을 계랑화
두 확률 변수가 독립인 경우 0

Ex) 사용 방법
window = 2인 단어 - 문맥 행렬

### 분포의 의미
1. 형태소 (morpheme)
의미를 갖는 최소 단위
Ex) 계열 관계
2. 품사



# MISSION
1. 붓꽃의 품종 분류하기
2. 손글씨 숫자 인식하기








