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

### **3.1 Basic data types**
다른 프로그래밍 언어들처럼, 파이썬에는 정수, 실수, 불리언, 문자열 같은 기본 자료형이 있습니다. 파이썬 기본 자료형 역시 다른 프로그래밍 언어와 유사합니다.

<br>

#### **3.1.1. Numbers**
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

파이썬 역시 long 정수형과 복소수 데이터 타입이 구현되어 있습니다. 자세한 사항은 다음 문서에서 확인할 수 있습니다. [링크](https://docs.python.org/3.7/library/stdtypes.html#numeric-types-int-float-long-complex).

<br>

#### **3.1.2. Boolean**
파이썬에는 논리 자료형의 모든 연산자가 구현되어 있습니다. 그렇지만 기호 (&&, ||, etc.) 대신 영어 단어로 구현되어 있습니다 :

``` python
t, f = True, False
print(type(t))
```
```
<class 'bool'>
```

<br>

``` python
print(t and f) # Logical AND;
print(t or f)  # Logical OR;
print(not t)   # Logical NOT;
print(t != f)  # Logical XOR;
```
```
False
True
False
True
```

<br>

#### **3.1.3. Strings**

``` python
hello = 'hello'   # String literals can use single quotes
world = "world"   # or double quotes; it does not matter
print(hello, len(hello))
```
```
hello 5
```

<br>

``` python
hw = hello + ' ' + world  # String concatenation
print(hw)
```
```
hello world
```

<br>

``` python
s = "hello"
print(s.capitalize())  # Capitalize a string
print(s.upper())       # Convert a string to uppercase; prints "HELLO"
print(s.replace('l', '(ell)'))  # Replace all instances of one substring with another
print('  world '.strip())  # Strip leading and trailing whitespace
```
```
Hello
HELLO
he(ell)(ell)o
world
```

<br>

모든 문자열 메소드는 다음 링크에서 확인할 수 있습니다. [링크](https://docs.python.org/3.7/library/stdtypes.html#string-methods).

<br>

### **3.2. Containers**
파이썬은 다음과 같은 컨테이너 타입이 구현되어 있습니다: 리스트, 딕셔너리, 집합, 튜플 등

<br>

#### **3.2.1. Lists**
list는 파이썬에서 배열 같은 존재입니다. 그렇지만 배열과 달리 크기 변경이 가능하고 **서로 다른 자료형**일지라도 하나의 list에 저장될 수 있습니다:

``` python
xs = [3, 1, 2]   # Create a list
print(xs, xs[2])
print(xs[-1])     # Negative indices count from the end of the list; prints "2"
```
```
[3, 1, 2] 2
2
```

<br>

``` python
xs[2] = 'foo'    # Lists can contain elements of different types
print(xs)
```
```
[3, 1, 'foo']
```

<br>

``` python
# Add a new element to the end of the list
xs.append('abc')
print(xs)
```
```
[3, 1, 'foo', 'abc']
```

<br>


``` python
x = xs.pop()     # Remove and return the last element of the list
print(x, xs)
```
```
bc [3, 1, 'foo']
```

<br>

#### **3.2.2. Slicing**
리스트의 요소로 한 번에 접근하는 것 이외에도, 파이썬은 리스트의 일부분에만 접근하는 간결한 문법을 제공합니다; 이를 슬라이싱이라고 합니다:

``` python
nums = list(range(5))    # range is a built-in function that creates a list of integers
print(nums)         # Prints "[0, 1, 2, 3, 4]"
print(nums[2:4])    # Get a slice from index 2 to 4 (exclusive); prints "[2, 3]"
print(nums[2:5])     # Get a slice from index 2 to the end; prints "[2, 3, 4]"
print(nums[0:2])     # Get a slice from the start to index 2 (exclusive); prints "[0, 1]"
print(nums[0:5])       # Get a slice of the whole list; prints ["0, 1, 2, 3, 4]"
```
```
[0, 1, 2, 3, 4]
[2, 3]
[2, 3, 4]
[0, 1]
[0, 1, 2, 3, 4]
```

<br>

#### **3.2.3. Loops**
아래와 같이 리스트의 요소들을 반복해서 조회할 수 있습니다

``` python
animals = ['cat', 'dog', 'monkey']
for animal in animals:
    print(animal)
```
```
cat
dog
monkey
```

<br>

만약 반복문 내에서 리스트 각 요소의 인덱스에 접근하고 싶다면, built-in enumerate 함수를 사용하세요:

``` python
animals = ['cat', 'dog', 'monkey']
for idx, animal in enumerate(animals):
    print('#{}: {}'.format(idx + 1, animal))
```
```
#1: cat
#2: dog
#3: monkey
```

<br>

#### **3.2.4. List comprehensions**
프로그래밍을 하다 보면, 자료형을 변환해야 하는 경우가 자주 있습니다. 간단한 예를 들자면, 숫자의 제곱을 계산하는 다음의 코드를 보세요.

``` python
nums = [0, 1, 2, 3, 4]
squares = []
for x in nums:
    squares.append(x ** 2)
print(squares)
```
```
[0, 1, 4, 9, 16]
```

list comprehension을 이용해 위 코드를 더 간단하게 만들 수 있습니다:

<br>

``` python
nums = [0, 1, 2, 3, 4]
squares = [x ** 2 for x in nums]
print(squares)
```
```
[0, 1, 4, 9, 16]
```

<br>

#### **3.2.5. Dictionaries**
Java의 ‘map’과 유사하게, Python의 ‘dictionary’는 (key, value) 쌍을 저장합니다. 아래와 같은 방식으로 dictionary 사용할 수 있습니다.

``` python
d = {'cat': 'cute', 'dog': 'furry'}  # Create a new dictionary with some data
```

<br>

``` python
print(d[0])
```
```
---------------------------------------------------------------------------
KeyError                                  Traceback (most recent call last)
<ipython-input-78-c7332189be96> in <module>()
----> 1 print(d[0])

KeyError: 0
```

<br>

``` python
print(d['cat'])       # Get an entry from a dictionary; prints "cute"
print('cat' in d)     # Check if a dictionary has a given key; prints "True"
```
```
cute
True
```

<br>

``` python
d['fish'] = 'wet'    # Set an entry in a dictionary
print(d['fish'])      # Prints "wet"
```
```
wet
```

<br>

``` python
print(d)
```
```
{'cat': 'cute', 'dog': 'furry', 'fish': 'wet'}
```

<br>

``` python
print(d['monkey'])  # KeyError: 'monkey' not a key of d
```
```
---------------------------------------------------------------------------
KeyError                                  Traceback (most recent call last)
<ipython-input-82-78fc9745d9cf> in <module>()
----> 1 print(d['monkey'])  # KeyError: 'monkey' not a key of d

KeyError: 'monkey'
```

<br>

``` python
print(d.get('monkey', 'N/A'))  # Get an element with a default; prints "N/A"
print(d.get('fish', 'N/A'))    # Get an element with a default; prints "wet"
```
```
N/A
wet
```

<br>

``` python
del d['fish']        # Remove an element from a dictionary
print(d)
print(d.get('fish', 'N/A')) # "fish" is no longer a key; prints "N/A"
```
```
{'cat': 'cute', 'dog': 'furry'}
N/A
```

만약 key와, 그에 상응하는 value에 접근하고 싶다면, ‘items’ 함수를 사용하세요:

<br>

``` python
d = {'person': 2, 'cat': 4, 'spider': 8}
for animal, legs in d.items():
    print('A {} has {} legs'.format(animal, legs))
```
```
A person has 2 legs
A cat has 4 legs
A spider has 8 legs
```

<br>


#### **3.2.6. Sets**
set은 순서 구분이 없고 서로 다른 요소 간의 모임입니다.

``` python
animals = {'cat', 'dog'}
print('cat' in animals)   # Check if an element is in a set; prints "True"
print('fish' in animals)  # prints "False"
```
```
True
False
```

<br>

``` python
animals.add('fish')      # Add an element to a set
print(animals)
print('fish' in animals)
print(len(animals))       # Number of elements in a set;
```
```
{'cat', 'dog', 'fish'}
True
3
```

<br>

``` python
animals.add('cat')       # Adding an element that is already in the set does nothing
print(len(animals))       
animals.remove('cat')    # Remove an element from a set
print(len(animals)) 
```
```
3
2
```

<br>

#### **3.2.7. Tuples**
tuple은 요소 간 순서가 있으며 값이 변하지 않는 리스트입니다. 

``` python
t = (5, 6)       # Create a tuple
print((t))
t[1] = 0    # Cannot change tuple values
```
```
(5, 6)
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-89-684b8a5f0477> in <module>()
      1 t = (5, 6)       # Create a tuple
      2 print((t))
----> 3 t[1] = 0    # Cannot change tuple values

TypeError: 'tuple' object does not support item assignment
```

<br>

<br>

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