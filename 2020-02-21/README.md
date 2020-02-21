# 영화 리뷰 분류와 IMDB dataset
2020-02-21-FRI

## 1-1. 완전연결신경망 
fully connected neural network

* ch6-0.ipynb
**Downgrade** 해야 함 ㅠㅠㅠ



#### 1. 훈련 데이터와 테스트 데이터 할당 
num_words=10000

#### 2. 영화 리뷰 샘플

#### 3. 데이터 전처리
```python
astype('float32')
```

#### 4. 신경망 모델
```python
model = models.Sequential()
model.add(layers.Dense(16, activation='relu', input_shape=(10000,)))
model.add(layers.Dense(16, activation='relu'))
model.add(layers.Dense(16, activation='sigmoid')) # 확률적 추정 시 사용

model.compile(optimizer='rmsprop', # 최적화 함수
							loss='binary_crossentropy', # 이진 분류
							metrics=['accuracy']) # 어떤 기준으로 결과가 나온 것을 평가할 것인지
```

##### output = relu(dot(`W`, input) + b)

- weight

#### 5. 훈련 검증
```python
history = model.fit(partial_x_train,
										partical_y_train,
										epochs=20, # loop
										batch_size=512,
										validation_data=(x_val, y_val)) # 검증 데이터 별도로
```
`loss` , `acc` (train data), `val_loss`, `val_acc` (validation data), 4개의 값


#### 과대 적합 overfitting
- 제어 파라미터, 데이터 수가 너무 많을 때 발생
- 복잡한 함수 적용했을 때 발생

#### 6. 단계 훈련도

#### 7. 과대 적합을 방지하기 위해 epochs=4로 제한
test data를 오염시키지 않는 것이 철칙

#### 8. 훈련된 모델로 예측



### 실습!
- 층의 hidden unit 수를 늘려보자
- 2개에서 3개로 hidden layer를 늘려보자



---
### 1. One-hot encoding
i번째 원소만 1이고, 나머지 원소는 모두 0인 벡터로 변환
- One-hot hashing
메모리를 적게 차지하도록 
`Sparse`, `hight-dim vector`
`Hard-coded`

### 2. Word Embedding
밀집 데이터로 나타내는 것, mapping
```python
import 
```
`Dense`, `low-dim vector`
`Learned from data`

---



## 1-2. IMDB dataset을 사용한 embedding
ch6-1.ipynb

```python
model = add(Embedding(10000, 8, input_length=maxlen))
# 완전 연결 신경망 층에 연결하기 위해 펼치는 것이 필요
model.add(Flatten())
```
각 단어를 독립적으로 취급
-> 단어 간 관계나 문장 구조를 전혀 고려하지 않음.
-> 학습 과정에서 sequence에 포함도니 단어 관계를 고려하도록 함
-> 임베딩 층 위에 순환층 (RNN)이나 CNN층을 추가하는 것이 필요!



ch6-2.ipynb (**읽어보기~!**)
#### 1. IMDB dataset 다운로드

#### 2. 훈련 데이터 생성

#### 3. tokenizer

#### 4. 훈련, 검증 세트 분리

#### 5. Glove 다운로드

#### 6. parsing

#### 7. word embedding matrix 생성

#### 8. 모델 정의

#### 9. 모델에 GloVe 임베딩 적용
```python
model.layers[0].set
```

#### 10. 훈련 손실과 검증 손실

#### 11. 

#### 12. 훈련 샘플 수를 늘리면 
검증 정확도가 증가할 수 있다

#### 13. test data로 model 평가



## 2. simpleRNN

## 3. LSTM



## 4. CNN

glovalMaxPooling

























