# 다양한 모델을 사용한 영화 리뷰 IMDB 처리
2020-02-13-THU

## 1. 완전연결신경망 
fully connected neural network
with keras

### 1) without word embedding
1. 데이터 전처리 (NLP에서 가장 중요한 과정)
2. 신경망 모델
3. 훈련 검증
4. 훈련 정확도 및 검증 정확도



- **임베딩이 크게 중요한 요소는 아니다!**



### 2) IMDB dataset을 사용한 embedding
1) Word2vec
2) GloVe: Wikipedia, Common Crawl 데이터, [50, 100, 200, 300]차 Embedding vector
과대 적합(over fitting)이 빠르게 시작



---
- `simpleRNN`, `LSTM`은 sequence 처리에 적합



## 2. simpleRNN
여러 개의 층을 만들어서 구현하는 방식
시간이 좀 소요되는 편이지만 validation accuracy 85%

## 3. LSTM
```python
from keras.layers import LSTM
```
시간이 더 소요, 검증 정확도 88%
NLP보다는 번역에 효과적



---



## 4. CNN
합성곱(Convnet)
* pooling 기법 (technique)



# NLP
**1. training data, 2. validation data, 3. test data 각각  분리**하는 것 중요!



#### c.f.
- 적대적 신경망
- Google News vector negative 300
- tensorflow hard coding
- Google Colab / Server



















