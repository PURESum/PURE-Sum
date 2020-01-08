# Day 2: Numpy, pandas

## Numpy
dtype, astype(형변환)
index, slicing

isnan(not a number - 상수)

```python
import matplotlib.pyplot as plt

# 기계학습 regration
np.random.random((1000,1))

# classification
plt.plot(x_test, y_test, 'bo')
```

## Pandas
table 형태의 대형 데이터를 다루는 것이 편리한 라이브러리이다.
data analysis에서의 핵심으로 굉장히 편리하게 데이터를 다룰 수 있다.
1. Series
2. DataFrame: Dictionary 객체와 같다고 보면 된다.

```python
import pandas as pd
# 1. Series
# scala 값
# vaules, indexes
obj = pd.Series([4, 7, 5, 3])

# 2. DataFrame
# 2차원
# rows, columns
frame = pd.DataFrame(data)
```

* 웹사이트 스크레이핑 후 **pandas**를 이용하여 테이블 형식으로 데이터를 관리하면 좋을 것!

#### ffill
outliner 데이터들을 처리할 때 유용



### Practices
gdp가 높은 나라가 삶의 만족도가 높은가?
-> 두 분류의 데이터를 결합시켜 추정해보는 예제

#### loc, iloc
특정한 데이터를 가져오는 것


## 자연어 처리
### 한글 - 유사도 처리
- 문장의 감정 표현 추정
ex) 가가 가가?, 라떼
문장의 키워드를 찾기 위해 품사 분류
**명사**와 **동사** 가 핵심적인 역할 (형용사는 제외)
문장구조를 확실하게 분류하기 보다, 문장 내에서 어떤 의미를 가지는지! 유사도를 이용한 처리
- 명사 구 처리
ex) **겁을 먹은 토끼**가 달아났다.
- 챗봇
- Numpy, Pandas: 데이터 처리
- Matplotlib: 시각화
- RNN, GAN(경쟁 모델), AutoIncoder
- NLTK 기반: 교수님 세미나 진행 예정
















