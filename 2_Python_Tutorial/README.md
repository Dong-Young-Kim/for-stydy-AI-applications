# Python Tutorial With Google Colab

## 1. Introduction

### 다루는 내용:

- Basic Python: Basic data types (Containers, Lists, Dictionaries, Sets, Tuples), Functions, Classes
- Numpy: Arrays, Array indexing, Datatypes, Array math, Broadcasting

<br>

## 2. A Brief Note on Python Versions
현재 파이썬에는 파이썬2와 파이썬3의 두 가지 버전이 있습니다. 파이썬2의 최종 버전은 파이썬 2.7이며, 파이썬3은 계속 버전이 증가하고 있습니다. 혼란스럽게도, 파이썬3은 기존 파이썬2와 호환되지 않게 변경된 부분이 있습니다. 그러므로 파이썬 2.7로 쓰여진 코드는 파이썬3 환경에서 동작하지 않고 그 반대도 마찬가지입니다.

```bash
!python --version
```
```bash
Python 3.7.12
```

<br>

## 3. Basics of Python

### 3.1 Basic data types
다른 프로그래밍 언어들처럼, 파이썬에는 정수, 실수, 불리언, 문자열 같은 기본 자료형이 있습니다. 파이썬 기본 자료형 역시 다른 프로그래밍 언어와 유사합니다.

<br>

### 3.1.1. Numbers
다른 언어와 마찬가지로 파이썬의 정수형(Integers)과 실수형(floats) 데이터 타입 역시 동일한 역할을 합니다:

``` python
x = 3
print(x, type(x))
```
```
3 <class 'int'>
```

<br>

``` python
print(x + 1)   # Addition
print(x - 1)   # Subtraction
print(x * 2)   # Multiplication
print(x ** 2)  # Exponentiation
```
```
4
2
6
9
```

<br>

``` python
x += 1
print(x)
x *= 2
print(x)
```
```
4
8
```

<br>

``` python
y = 2.5
print(type(y))
print(y, y + 1, y * 2, y ** 2)
```
```
<class 'float'>
2.5 3.5 5.0 6.25
```

<br>

다른 언어들과는 달리, 파이썬에는 증감 단항연산자(x++, x--)가 없습니다.

파이썬 역시 long 정수형과 복소수 데이터 타입이 구현되어 있습니다.


``` python

```
```

```

## 3.3. Functions
파이썬 함수는 def 키워드를 통해 정의됩니다.

``` python
def sign(x):
    if x > 0:
        return 'positive'
    elif x < 0:
        return 'negative'
    else:
        return 'zero'

for x in [-1, 0, 1]:
    print(sign(x))
```
```
negative
zero
positive
```

<br>

<span style="color:grey"> *인하대학교 '인공지능응용(ICE4104)' 강의를 기반으로 작성된 문서입니다.*</span>

---