# 딥러닝 기초

# 인공 신경망 Artificial Neural Network
input x weight 누적 합이 threshold 보다 크면 neuron이 fire / activate (발화 / 활성화)

- 계단 함수 step function
- perceptron
- `ReLU`
- `sigmoid`: 양 끝에서 포화 (saturate), 부드럽게 변화 -> 확률적 판단 시 사용

### Delta Rule

## 신경망 학습
개와 고양이 분류

## 학습 방법
1. 지도 학습 Supervised learning
2. 비지도 학습 Unsupervised learning
3. 강화 학습 Reinforcement learning

## 학습 과정
1. 학습 데이터 준비 (전처리)
2. 데이터를 입출력 데이터로 구분
3. 신경망에 데이터를 입력
4. 판정 결과와 출력 데이터 비교
5. 차이를 feedback
6. parameter 갱신 -> goto 3

### Loss Function 손실 함수
- Mean Squared Error 평균 제곱 오차
- Cross Entropy Error 교차 엔트로피 오차  
	- `one-hot-vector`: 확률과 관련이 있음, 본인에 해당되는 것에만 초점을 맞추어 판정하는 방식, 완만한 단조 감소 함수 monotonic decreasing function
	- entropy: 정보를 최적으로 인코딩하기 위해 필요한 비트 수

### 신경망의 파라미터 조정: Gradient method 경사법
- Optimization Problem 최적화 문제
경사 하강법, 뉴튼법, 경사 하강법, momentum (RMSProp, Adam)

- Back Propagation 오차 역전파

## 손글씨 숫자 인식하기
MNIST



















