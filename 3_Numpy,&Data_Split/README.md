# Numpy & Data Split

## 1. Numpy
파이썬은 자체 베열 자료형을 제공하지 않아, 배열을 구현한 다른 패키지를 inport 해야 한다. 파이썬에서 배열을 사용하기 위한 표준 패키지는 **Numpy** 이다.

> **Numpy**는 파이썬이 계산과학분야에 이용될때 핵심 역할을 하는 라이브러리이다. Numpy는 **고성능의 다차원 배열 객체**와 이를 다룰 도구를 제공한다.

Numpy를 사용하기 위해서는 먼저 numpy 패키지를 import해야 한다.

```python
import numpy as np
```

np는 numpy package를 np로 쉽게 불러 사용하기 위해서 위와 같이 작성한다.

### 1.1 Arrays

Numpy 배열은 **동일한 자료형**을 가지는 값들이 격자판 형태로 배열된 것이다. 각각의 값들은 tuple(이때 tuple은 양의 정수만을 요소값으로 갖는다) 형태로 색인된다.

파이썬의 리스트를 중첩해 Numpy 배열을 초기화 할 수 있고, 대괄호를 통해 각 요소에 접근할 수 있다.

<br>

```python
a = np.array([1, 2, 3])  # Create a rank 1 array
print(type(a))
print(a.shape)
print(a[0], a[1], a[2])

# Change an element of the array
# [5 2 3]
a[0] = 5
print(a)      
```
```
<class 'numpy.ndarray'>
(3,)
1 2 3
[5 2 3]
```

<br>

```python
b = np.array([[1,2,3],[4,5,6]])   # Create a rank 2 array
print(b)    
```
```
[[1 2 3]
 [4 5 6]]
```

<br>

rank는 배열이 몇 차원인지를 의미합니다. 
shape는 각 차원의 크기를 알려주는 정수들이 모인 tuple입니다.

```python
print(b.shape)
print(b[0, 0], b[0, 1], b[1, 0])  
```
```
(2, 3)
1 2 4
```

<br>

Numpy는 배열을 만들기 위한 다양한 함수를 제공합니다.

**zeros**

```python
a = np.zeros((2,2))  # Create an array of all zeros
print(a)
```
```
[[0. 0.]
 [0. 0.]]
```

<br>

**ones**

```python
b = np.ones((1,2))   # Create an array of all ones
print(b)
```
```
[[1. 1.]]
```

<br>

**full**

```python
c = np.full((2,2), 3) # Create a constant array
print(c)
```
```
[[3 3]
 [3 3]]
```

<br>

**eye**

```python
d = np.eye(2)        # Create a 2x2 identity matrix
print(d)
```
```
[[1. 0.]
 [0. 1.]]
```

<br>

**random**

```python
e = np.random.random((2,2)) # Create an array filled with random values
print(e)
```
```
[[0.68326352 0.60999666]
 [0.83319491 0.17336465]]
```

<br>

### Array Indexing

Numpy는 배열을 인덱싱하는 몇 가지 방법을 제공한다

> Slicing: 파이썬 리스트와 유사하게, Numpy 배열도 슬라이싱이 가능하다. Numpy 배열은 다차원인 경우가 많기에, 각 차원별로 어떻게 슬라이스할건지 명확히 해야 합니다:

<br>

<span style="color:grey"> *인하대학교 '인공지능응용(ICE4104)' 강의를 기반으로 작성된 문서입니다.*</span>

---