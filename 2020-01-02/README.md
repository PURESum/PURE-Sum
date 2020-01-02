# Day 1: Numpy
Prepared by Prof. Youn-Sik Hong
2020.12.02



빅데이터 클러스터 연구단 - 동영상 강의 제작 예정
데이터를 핸들링하는 라이브러리



## Python 기본
* Python
  - tuple
  - list
  - dictionary
  - set

* jupyter notebook 사용법

* utility function
  - sorted
  - zip: 여러개의 리스트를 합쳐서 반환
  - reversed
  - **enumerate**: for 루프에서 index와 value를 한번에 처리
```python
for index, name in enumerate(my_list):
  print(format(index, name))
```

* 함수
  - 정의: def
  - 다수의 리턴 값: return a, b, c
  - generator
  - **lamda expression**
```python
double_values(my_values, labmda x:x+x)
```

* file I/O
  - open(path)
  - f.close
  - with open(path) as f:

## Numpy
Numerical Python의 약자
array, 수학 연산에 강력한 기능, python보다 10배 빠른 속도
다차원 배열 (4차 이상) 처리

### Numpy ndarray
```python
import numpy as np # numpy library
my_arr = np.arange(10000000) # 정수 배열
%time for _ in rage(10): my_arr2 = my_arr * 2 # 25.9ms

my_list = list(range(1000000))
%time for _ in range(10): 
```

```python
data = np.random.randn(2, 3) #0에서 1 사이에 있는 랜덤 실수
# randn은 정규 분포를 따르는 값을 생성함.
data.shape # (2, 3)
data + data # 배열 각 원소에 *2 한 결과와 같다.
```

### Arrays
```python
a = np.array([[1, 2, 3], [4, 5, 6]], dtype=np.float32)
print(a.ndim, a.shape, a.dtype)
# 2 (2, 3) float32
```

```python
np.linsape(0, 10, 25)
np.logspace(0, 10, 10, base=np.e)
np.diag([1, 2, 3])

np.zeros(10) # 1차원 배열
np.zeros((3, 6)) # 2차원 배열
np.empty((2, 3, 2)) # 3차원 배열
np.ones(10)
```

### index, slicing
```python
arr = np.arange(10) # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
arr[5] # 5
arr[5:8] # [5, 6, 7]
arr_slice[1] = 12345
arr_slice[:] = 64

arr_slice = arr[5:8].copy()
```

### select by Boolean value
```python
names = np.array(['Bob', 'Joe', ...])
data = np.random.randn(7, 4)

names == 'Bob'
data[names=='Bob']
```

### Fancy indexing

### Transpose (전치)
array vector matrix
2 x 3 -> 3 x 2
행렬의 곱셈: weight

```python
# transpose
arr = np.arange(15).reshape((3, 5))
arr = np.arange(16).reshape((2, 2, 4))
```

### ufunc: Universal function
Unary function
binary function



### expressing
```python
result = [(x if c else y) for x, y, c in zip(xarr, yarr, cond)] # python
result = np.where(cond, xarr, yarr) #numpy

arr = np.random.randn(4, 4) 
arr > 0 
np.where(arr > 0, 2, -2) #numpy
```

### axis
**axis = 1**, find the sum of each **column**
**axis = 0**, find the sum of each **row**
cumsum, cumprod
argmin, argmax



### self learning
- Array Creation functions
- basic operations
- select by slicing
- select by Boolean value
- Universal function













