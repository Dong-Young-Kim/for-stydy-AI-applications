# Basic Python

## 1. 데이터 분석용 파이썬 패키지

여러 분야 사용할 수 있는 다양한 패키지를 가지고 있다는 점은 파이썬의 큰 장점이다.


```
ㅇ NumPy
    - 수치해석 라이브러리
    - http://www.numpy.org/
    - 2006, Travis Oliphant
ㅇ SciPy
    - 과학기술 함수 라이브러리
    - http://www.scipy.org/
    - 2001, Travis Oliphant, Pearu Peterson
ㅇ SymPy
    - 심볼릭 연산 라이브러리
    - http://www.sympy.org/
    - 2006, Ondřej Čertík
ㅇ Matplotlib
    - 시각화 라이브러리, matlab 플롯 기능 구현
    - http://matplotlib.org/
    - 2002, John D. Hunter
ㅇ seaborn
    - 시각화 라이브러리. 통계용 차트 및 컬러맵 추가
    - https://stanford.edu/~mwaskom/software/seaborn/
    - 2012, Michael Waskom
ㅇ bokeh
    - 시각화 라이브러리. 웹상에서 인터액티브 플롯 구현
    - http://bokeh.pydata.org
    - 2012, Peter Wang
ㅇ pandas
    - 데이터 분석 라이브러리. R의 data.frame 자료구조 구현
    - http://pandas.pydata.org/
    - 2008, Wes McKinney (AQR Capital Management)
ㅇ statsmodels
    - 다변량 회귀 분석 및 시계열 분석 라이브러리
    - http://statsmodels.sourceforge.net/stable/
    - 2009, Skipper Seabold
ㅇ scikit-learn
    - 머신러닝 라이브러리
    - http://scikit-learn.org
    - 2007, David Cournapeau
ㅇ TensorFlow
    - 딥러닝 라이브러리
    - https://www.tensorflow.org/
    - 2015, google
ㅇ Keras
    - 고수준 딥러닝 라이브러리
    - https://keras.io/
    - 2015, François Chollet
```

<br>

## 2. 파이썬 조건문
### if ~ else 명령
주의할 점 : 참 또는 거짓일 때 실행되는 명령들은 앞 빈칸을 4칸 띄우고 써야 한다.
``` python
a = 10

if a % 2 == 0:
    print("짝수")
else:
    print("홀수")
```
``` bash
짝수
```
<br>

``` python
b = 55 #@param {type:"raw"}

if (b >= 10) & (b < 100) & (b % 2 == 0):
    print("2자리수의 짝수이다.")
else:
    print("2자리수의 짝수가 아니다.")
```
``` bash
2자리수의 짝수가 아니다.
```
<br>

``` python
c = 6

if c >= 8:
    print("A")
elif c >= 5:
    print("B")
else:
    print("C")
```
``` bash
B
```
<br>

``` python
sex_cd = 'M'  #@param {type:"raw"}
pushup = 8  #@param {type:"raw"}

if sex_cd == "M":
    if pushup >= 10:
      grade = "Pass"
    else:
      grade = "Fail"
else:
    if pushup >= 5:
      grade = "Pass"
    else:
      grade = "Fail"

print(grade)
```
``` bash
Fail
```
<br>

<br>

<span style="color:grey"> *인하대학교 '인공지능응용(ICE4104)' 강의를 기반으로 작성된 문서입니다.*</span>

---