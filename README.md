# colab_upload

# 사이드 프로젝트 : 크롤링 
- - - 

 * 1. 네이버 쇼핑 API를 통한 쇼핑 인사이트 
 * 2. 공공데이터 포털 API 파싱
   

   * 2-2. 한국문화관광연구원 _ 출입국관광통계서비스 내 중국인 출입 현황 그래프

       ![결과그래프](./images/다운로드.png)
* 3. 네이버 검색 트렌드 API를 통한 파싱
  * 3-1. 대한민국 3대 대형은행 (농협,신한,국민) 날짜별 검색 현황
  

  * 3-2. 쇼핑때와는 다르게 일률적으로 분포되어 있는 것을 확인
     ![결과그래프](./images/은행_그래프.png)
 - - - 
 
  
파이썬 기초 1 

초기 세팅 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/edf52975-9cda-49b5-8df5-e8e7f854f507/Untitled.png)

![기본적인 머신러닝을 위해 GPU로 변경](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2f47aebe-f8d2-4862-9766-1917a6d1c72c/Untitled.png)

기본적인 머신러닝을 위해 GPU로 변경

## 01. 🍟변수란?

자료를 넣는 상자 

어떤 자료를 담느냐에 따라 상자의 모양 / 성격(자료형)이 달라짐

```python
a = 1 
b = 3.14
c = "ㄱ" # str 문자형은 반드시 따옴표를 넣어야한다 

print(type(a))
print(type(b))
print(type(c))
```

### 문자의 특성

문자 1개 = 문자 

문자 2개 이상 = 문자열

문자열은 순서가 있고 번호를 불러 그 번호에 해당하는 문자를 꺼내올 수 있다.

Python에서 문자열의 길이(문자열에 포함된 문자의 개수)는 내장 함수 `len()`을 이용하여 구할 수 있다.

예를 들어, 아래와 같은 문자열의 길이를 구할 수 있다.

```python
str = "Hello World"
print(len(str))  # 11 출력

```

또한, 문자열 메서드 `count()`를 이용하여 특정 문자나 문자열이 문자열 내에 몇 개 존재하는지 세어볼 수도 있다.

```python
str = "Hello World"
print(str.count('l'))   # 3 출력
print(str.count('lo'))  # 1 출력

```

### 변수의 특징

변수에는 1개의 자료만이 들어갈 수 있다.

변수에 다른 자료를 넣으면 이전 자료는 사라지게 된다. 

---

### 변수 삭제하기

```python
del # 변수를 삭제시키는 명령어
```

### 키보드 값을 입력 받아 변수에 저장하기

```python
num = int(input('갑 입력>>'))
print(num)
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/15db0aa4-9539-4419-aba6-260460037bd4/Untitled.png)

---

**형 변환**

- 데이터 타입을 변환 시켜준다
- int - 정수 : int(변수명)
- float 실수 : float(변수명)
- str 문자/문자열 : str(변수명)

---

**문자와 문자열**

- 문자형 변수에는 단어 뿐만 아니라 문장도 들어갑니다

---

**리스트형 변수 - 데이터 분석에서 가장 많이 사용하는 자료형 1**

- 모든 데이터 타입(정수,실수,문자열,리스트,딕셔너리)의 자료를 넣을 수 있다.
- 리스트 자료형은 순서기 있는 자료형이다
- 순서가 있는 자료형은 index(번호)로 자료를 꺼낼 수 있다.
- 리스트 자료형식은 [자료1,자료2,자료3] 형식을 만든다

---

**슬라이싱 : 리스트에서 범위를 지정해 자료를 여러개 가져오는 법**

- 변수명[시작번호:끝번호 바로 앞까지 범위]
- 변수명[시작번호:끝번호 바로 앞까지:범위간격]

---

**튜플**

- 튜플을 리스트와 거의 동일
- 차이점은 리스트 대괄호 [] 튜플은 () 괄호로 포장
- 리스트는 자료의 변경이 가능하나 튜플은 변경이 불가능하다
- 리스트보다 속도가 빠르기 때문에 쓰인다

---

**딕셔너리  : JSON이라고도 함**

데이터분석에서 가장 많이 사용되는 자료형2

- key : value 형태의 자료형으로 나중에 API를 이용해서 자료를 수집하면 대부분 JSON 형태로 받게된다.
- 변수명 = {key:value, ....}
- Value = 모든 자료형이 올 수 있다.

## 🌭연산자의 종류와 활용

1) 연산자의 종류

1-1) 더하기 

1-2) 빼기 

1-3) 곱하기

1-4) 나누기 

1-5) 나머지

*) 나누기를 하면 나머지가 타입이 실수로 변한다

**할당 연산자**

- =,+=,-=,*=,/=,%=

**괄호 사용법**

연산자 우선순위 : () 안쪽이 연산에서 우선 순위를 갖는다

**할당 연산자**

- =,+=,-=,*=,/=,%=

**비교연산자 ==,!= , >,<,>=,<=**

- 항상 왼쪽을 기준으로 비교

**!= 다르면 True, 같으면 False**

> 왼쪽을 기준으로 왼쪽 값이 오른쪽보다 큰것인가?

**식별 연산자 : is,is not - 객체(object)가 같은지 비교**

**논리 연산자**

- and, or , not not
- and는 비교 하는 두 값 모두가 참이어야 참이 된다 .

**1. 산술 연산자(arithmetic operator)**

**기본적인 산술 연산을 위해 제공되는 연산자이다.**

| + | 왼쪽 항에 오른쪽 항을 더한다 |
| --- | --- |
| - | 왼쪽 항에 오른쪽 항을 뺀다 |
| * | 왼쪽 항에 오른쪽 항을 곱한다 |
| / | 왼쪽 항을 오른쪽 항으로 나눈다 |
| % | 왼쪽 항을 오른쪽 항으로 나눈 나머지 |
| ** | 왼쪽 항에 오른쪽 항만큼 제곱한다 |
| // | 왼쪽 항을 오른쪽 항으로 나눈 몫 |

**2. 대입 연산자(assignment operators)**

| = | 왼쪽 항에 오른쪽 항을 대입한다 |
| --- | --- |
| += | 왼쪽 항에 오른쪽 항의 값을 더하고 왼쪽 항에 대입한다 |
| -= | 왼쪽 항에 오른쪽 항의 값을 빼고 왼쪽 항에 대입한다 |
| *= | 왼쪽 항에 오른쪽 항의 값을 곱하고 왼쪽 항에 대입한다 |
| /= | 왼쪽 항을 오른쪽 항의 값으로 나누고 왼쪽 항에 대입한다 |
| %= | 왼쪽 항을 오른쪽 항의 값으로 나눈 나머지를 왼쪽 항에 대입한다 |
| **= | 왼쪽 항에 오른쪽 항의 값만큼 제곱하고 왼쪽 항에 대입한다 |
| //= | 왼쪽항을 오른쪽 항의 값으로 나눈 몫을 왼쪽 항에 대입한다 |

**3. 비교 연산자(comparison operator)**

**값의 크기를 비교하는 연산자이다. C++의 경우 값을 비교하여 참일 경우 1을 거짓일 경우 0을 반환했지만 파이썬은 참일 경우 True를 거짓일 경우 False의 bool형 값을 그대로 반환한다.**

| == | 왼쪽항과 오른쪽 항의 값이 같을 경우 참 |
| --- | --- |
| != | 왼쪽항과 오른쪽 항의 값이 다를 경우 참 |
| > | 왼쪽항이 오른쪽 항보다 큰 경우 참 |
| < | 왼쪽항이 오른쪽 항보다 작은 경우 참 |
| >= | 왼쪽항이 오른쪽 항보다 크거나 같을 경우 참 |
| <= | 왼쪽항이 오른쪽 항보다 작거나 같을 경우 참 |

**4. 논리 연산자(logical operator)**

**주어진 논리 식의 참(True) 거짓(False)을 판단한다.**

| and | 두 항을 비교하여 둘다 참일 경우 참을 반환 한다 |
| --- | --- |
| or | 두 항을 비교하여 둘중 하나라도 참인 경우 참을 반환 한다. |
| not | 논리 결과를 반전시킨다. |

| x | y | x and y | x or y | not(x) |
| --- | --- | --- | --- | --- |
| T | T | T | T | F |
| T | F | F | T | F |
| F | T | F | T | T |
| F | F | F | F | T |

**5. 비트 연산자(bitwise operator)**

**비트단위 논리 연산을 진행할 때 사용한다. 만약 a가 30일 경우 0001 1110으로 b가 5일 경우 0000 0101로 바꾸어 비교하는 것이다.**

| & | 두항의 비트를 비교 같은 자리의 비트가 모두 1일 경우 1을 반환 (비트AND) |
| --- | --- |
| | | 두항의 비트를 비교 같은 자리의 비트중 1이 존재할 경우 1을 반환 (비트 OR) |
| ^ | 두항의 같은 자리의 비트가 서로 다를 경우 1을 반환 (비트 XOR) |
| ~ | 비트가 1일 경우 0으로, 0일 경우 1로 반환 (비트 NOT, 1의 보수) |
| << | 지정한 수만큼 비트를 왼쪽으로 이동 (left shift) |
| >> | 지정한 수만큼 비트를 오른쪽으로 이동 (right shift) |

**6. 멤버 연산(membership operator)**

**멤버 연산자의 경우 list안에 확인하고자 하는 값이 들어가 있는지에 대한 여부를 확인할 때 사용한다.**

| in | 왼쪽항이 오른쪽 리스트 안에 들어 있으면 참 |
| --- | --- |
| not in | 왼쪽항이 오른쪽 리스트 안에 안들어 있으면 참 |

**※연산자 우선 순위**

| ** | 지수 |
| --- | --- |
| ~ + - | 보수, 양수와 음수 |
| * / % // | 곱하기, 나누기, 나머지, 몫 |
| + - | 덧셈과 뺄셈 |
| >> << | 좌우 비트 시프트 |
| & | 비트 'AND' |
| ^ | | 비트  'XOR'와  'OR' |
| <= < > >= | 비교 연산자 |
| <> == != | 비교 연산자 |
| = %= /= //= -= += *= **= | 대입 연산자 |
| is is not | 식별 연산자 |
| in not in | 맴버 연산자 |
| not or and | 논리 연산자 |

---

## 🎴문자열

1. 문자열 사용하기 기본 
- ‘’,”” 인에 문자를 넣는다
- 작은 따옴표를 표시 하고자 하면 큰 따옴표로 감싸고
- 큰 따옴표를 표시하고자 하면 작은 따옴표로 감싼다

**이스케이프 문자**

() 사용하기 

- \n : 줄바꿈 new line
- \t : 탭
- \r : 캐리지리턴

---

**문자열 함수**

- 문자열을 조작하는 함수
- .split().join().strip().replace()
- split() : 기준 문자를 기준으로 문자열을 분리 리스트로 저장
- join() : 앞 쪽에 지정한 형식을 포함해서 문자열을 합쳐준다
- strip() : 문자열 양쪽 끝에 공백이나 특수문자를 제거
    - 단점 : 문자열 내부의 특수문자 및 공백을 제거하지 못함
- replace() : 문자열에서 원하는 값을 찾아 다른 값으로 변경
- split으로 쪼개진 요소는 list로 반환시켜준다
    - **그러므로 list 형태이므로 list 형태를 가진 요소에는 사용할 수 없다**
    - 
- split으로 쪼개진 부분을 붙여주는 방법

| 명칭 | 용도 |
| --- | --- |
| split |  기준 문자를 기준으로 문자열을 분리 리스트로 저장 |
| join | 앞 쪽에 지정한 형식을 포함해서 문자열을 합쳐준다 |
| strip |  문자열 양쪽 끝에 공백이나 특수문자를 제거 |
| replace | 문자열에서 원하는 값을 찾아 다른 값으로 변경 |

```python
L4 = ['사과','배','포도','파인애플']

','.join(L4)
```

‘,’.join() 컴마를 기준으로 → 붙여주겠다 라는 의미 

split(list) ↔ join(str) 

번갈아가면서 사용하는 것이 중요할 것 같다. 

replace(’찾을문자’,’바꿀문자’)


---
**Review**

**데이터 분석을 할 때 웹에서 가져오는 데이터는 기본적으로 문자열 형태가 많음**

### 문자열을 얼마나 잘 다루느냐 == 데이터 전처리 속도를 좌우 함

---

**1. 문자열 사용하기의 기본**

---

**' ' 따옴표 안에 문자을 넣는다. 큰따옴표 작은따옴표 모두 가능**

---

자주 쓰는 이스케이프 문자 \n(줄바꿈), \t(탭), \r(캐리지리턴-줄 맨 왼쪽으로 커서이동)

**인덱스와 문자열**

---

**문자열은 여러개의 문자가 줄을 선 것과 같이 이어진 글자의 모음이므로 왼쪽부터 번호를 매길 수 있음**

**인덱스를 활용한 문자열 슬라이싱**

---

위의 인덱스를 활용하면 문자열이 일부분만 잘라서 가져오는 슬라이싱이 가능합니다.

**2. 문자열 함수**

---

문자열을 조작하는데는 활용되는 여러가지 함수가 있습니다. 이 함수들을 잘 사용해야 데이터 전처리를 효과적으로 할 수 있습니다. 특히 .split(), .join(), .strip() 등의 함수들을 잘 익혀두시기 바랍니다.

---

**1) 문자열 바꾸기**

---

**.replace(a,b) a를 찾아 b로 바꿈 단, 원본은 바꾸지 않기 때문에 따로 저장 필요**

**2) 문자바꾸기**

### str.maketrans('바꿀문자','새문자', '추가로 없앨문자') 로 변환테이블 생성 후 translate로 문자를 찾아 바꿈

---

**range 함수와 list 형변환을 이용하여 리스트 만들기**

- range(시작번호 , 끝번호 + 1, 증가량)

```python
d = list(range(1,101,3)) # 1부터 100까지 숫자 중 3씩 건너뛰면서 만들어줘 
d
```

```python
e = list(range(3,101,3))
```

### 🧨sep! 옵션

프린트 출력시 구분단위이다 

```python
f = 10 
g = 20 
h = 30

print(f,g,h,sep=',')
10,20,30
```

(,) 콤마로 구분되어 출력이 된다. 

또한 end 옵션이 가능하다 

### 🧨end! 옵션

```python
print(f,end='\t')
print(g,end='\t')
print(h,end='\t')
10	20	30
```

결과들끼리의 간격이 늘어난다 tab~ 같은 느낌

---

## **append()**

- list에 자료를 추가하는 함수
- 자료는 어떤것을 넣든 상관은 없지만 가장 끝에 붙는다

```python
c = [10,20,30]
c
[10, 20, 30]
c.append(50)
c
[10, 20, 30, 50]
```

## insert()

- list의 특정 index에 자료를 추가
- insert(넣고싶은 index,무엇을 넣을지?)

```python
c.insert(3,40)
c
[10, 20, 30, 40, 50, 50]
```

- 삽입된 자료 뒤의 자료는 인덱스가 뒤로 밀리게 된다.

## extend()

- list뒤에 다른 list의 자료만 추가하는 함수

append와 비교 

```python
c = [10,20,30]
d  = [200,300,400,500]
c.append(d) 
[10,20,30,[200,300,400,500]] 

c.extend(d)
[10,20,30,[200,300,400,500],200,300,400,500]] 
```

append는 리스트를 통째로 추가해주고 

extend는 리스트 안의 자료들을 넣어준다 

---

## 🧤리스트의 삭제

- 리스트 내부의 자료를 한 개 삭제 할 때
- 리스트는 항상 인덱스로 접근한다

```python
del 변수명[인덱스]
.pop() # 마지막 인덱스를 출력 후 삭제해줌 
```

.pop() : 리스트의 가장 마지막 데이터를 출력 후 삭제

.pop(변수의 인덱스 번호) 로도 추출하여 삭제 시킬 수 있다. 

## remove()

- .remove(리스트 안의 값)
- remove는 리스트 내의 중복 자료가 있을 경우 앞 쪽 자료만 삭제된다.

## clear()

- 리스트 내부의 자료를 모두 삭제 시킴
- 변수 자체는 삭제시키지는 못함

## index()

- list에서 특정 값의 인덱스를 구하기
- .index(찾을값 , 시작번호, 인덱스 끝번호)

## count()

- list 안에서 원하는 값이 몇 개 있는지 찾아줌

## **list 정렬하는 방법**

- .sort() : default 가 오름차순 - 작은숫자 -> 큰 숫자
- .sort(reverse = True) : 내림차순 - 큰 숫자 -> 작은 숫자
- 실행 하자마자 원본에 재할당 (덮어쓰기가 됨) reverse와 비슷하니 조심

---

## 내장함수의 문제점

자동 할당으로 인해 실수 한 번이면 되돌릴 수 없는 부분들이 굉장히 큼 

그 부분을 해결 

---

## **sorted()**

- sorted(변수명)
- 변수의 재할당(덮어쓰기) 없이 오름차순으로 정렬 된 결과를 보여줌

---

### 리스트 튜플, 문자열의 공통점

- 순서가 있고 연속된 값이 들어있다.
- 이러한 연속적인 자료형을 시퀀스 자료형이라고 한다. (시퀀스 객체라고도 함)
- 시퀀스 객체 : list , tuple , string , range() 자료형

---

**1. 특정 값이 스퀀스 객체 내에 있는지 확인하기 .**

: in 시퀀스 객체 (list,tuple,string,range())

```python
7 in a
True
```

```python
s = '우리는 오늘 삼복 더위에서 파이썬을 공부 하고 있습니다.'
'삼복' in s
True 
```

**2. 특정 값이 없는지 확인 하기**

값 not in 시퀀스 객체 

```python
'삼계탕' not in s 
True
```

**3. 시퀀스 객체 연결하기**

- '+' 연산자로 연결이 가능하다.
- 단 , range는 불가능 하다.

```python
a = list(range(10))
b = list(range(10,20))
print(a,b)
# a,b를 더하려면 원래는 extend를 써야하지만 
c = a+b
c
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
```

**4. 시퀀스 객체 반복하기 : * 연산자 사용**

- range()는 불가

**5. 시퀀스 객체의 길이를 구하는 함수 : len()**

**6. 시퀀스 자료형에서 자료 추가 삭제는 list만 가능하다**

🎈 문자열을 인덱싱이 가능하지만 수정이 불가능하다

---

## dictionary

---

### **딕셔너리(JSON) 사용하기**

- key : value 형태로 만들어진 자료형으로 반드시 key를 호출해야 value를 사용한다

### 2. 딕셔너리 key의 자료형

- 문자열, 정수, 실수, 불린(True,False)
- key로 올 수 없는 경우가 있는데 : list, 딕셔너리는 올수가 없음

### **3. 딕셔너리 값의 자료형**

- 딕셔너리 값에는 모든 자료형이 올 수 있다.

```python
y = {'정수':100,'실수':13.5,'문자열':'문자열문자열','리스트':[1,2,3,4],
     '튜플':(5,6,7,8),'딕셔너리':{'key':'value'},'boolean':True}
```

### **4.빈 딕셔너리 만들기**

- d = {}
- d = dict()

### **5. dict()로 딕셔너리 만들기**

- dict(key1 = value1 , key2 = value2) 형식으로 만들기
- 주의할 점 : key 값에 '',""를 쓰면 안 된다.
- 단점 : key 값에는 문자열로만 통일해서 넣을 수 있다 기존 {} 중괄호 내에서는 상관 없었지만 dict 내에서는 그게 불가능 하다는 것.

## 🎁부록

## **2) dict([(key1,value1),(key2,value2)])**

- 리스트 안에 (key,value)의 튜플을 나열해서 만든다

```python
d2 = dict([('정수',100),('실수',13.5)])
d2
```

## **3) dict(zip([key1,key2,key3,value1,value2,value3~]))**

형식으로 만들기

- zip 함수를 사용하여 첫 번째 리스트 key로 두 번째 리스트를 value로 값을 매칭해서 합침

dict(zip(['문자열','리스트','튜플','딕셔너리','블린']))

```python
dict(zip(['문자열','리스트','튜플','딕셔너리','블린']))
```

---

### 딕셔너리 key와 value 값을 삭제하기

- del 변수명[key] : 삭제가능

### 딕셔너리에 key와 value를  추가

- 변수명[추가할 Key] = 추가할 Value
--------

## 🍕조건문

- 사용방법

```python
if # 조건식 : 
# 코드  (조건식이 참일 때) 
elif #조건식 : 
# 다른코드 (다른 조건이 참일 때) 
else :
# 나머지 조건들 (조건식이 거짓일 때)
```

### 🍟다중 조건문

**다중 조건문 사용**

- elif

```python

if # 조건문 :
  # 코드 ( 조건이 참일 때 실행 )
elif # 조건문2 :
  # 코드 ( 조건2가 참일 때 )
elif # 조건문3 :
  # 코드 ( 조건3가 참일 때 )
else :
  # 조건이 거짓일 때
```

## 🌭연습문제

**학점 판별 프로그램**

- 81-100 : A61-80 : B41-60 : C21-40 : D0 - 20 : F

```python
while True: 
  user_input = int(input('점수 입력 >> '))

  if (80 < user_input<=100):
    print('A')
    break
  elif (60 < user_input <= 80):
    print('B')
    break
  elif (40 < user_input <= 60):
    print('C')
    break
  elif(20< user_input <= 40):
    print('D')
    break
  elif(0<= user_input <= 20):
    print('F')
    break
  else:
    print("없는 점수입니다 다시 입력해주세요")
    continue
```

### **교통비 차감 프로그램**

표준 입력으로 나이(만 나이)가 입력 됩니다 (입력 값은 7 이상 입력됨 )

교통카드 시스템에서 시내버스 요금은 다음과 같으며 , 각 나이에 맞게 요금을 차감한 뒤 잔액이 출력되게 만드시오 (if,elif사용)

<aside>
💡 현재 교통카드에는 9,000원이 들어 있습니다

어린이 650원 (7세 이상 12세 이하)

청소년 1,050원 (13세 이상 18세 이하)

어른 (19세 이상) 1,250원

</aside>

```python
# 입력 받는 곳 
# 나이가 7살 이상이면 판별 
# 나이가 7살 이상이면 어린이,청소년,어른별로 교통카드에서 요금 차감 

pay = 9000
user_age = int(input('나이를 입력하세요 >> '))

if (7<=user_age<=12 ):
  print(f'잔액은 {pay-650}원 입니다')
elif (13<= user_age <=18):
  print(f'잔액은 {pay-1050}원 입니다')
elif user_age >= 20 :
  print(f'잔액은 {pay-1250}원 입니다')
```

### **파이썬 만의 if 조건문 작성방법**

```python
# 참일 때 입력할 값
if # 조건문 else # 거짓일 때 입력할 값
```

```python
a = int(input())
b = int(input())
True if a == b else False 
# pythonic 스러운 if문
```

---

## 🥩 반복문

- 반복문은 동일한 작업을 여러번 반복 해야 하는 경우에 사용한다.
- 반복문 종류 for , while
- for 반복횟수를 정해놓고 시작
- while은 반복 횟수가 정해져 있지 않은 경우 사용

```python
for /* 변수 */ in range :
  반복할 코드 

for 변수 in 시퀀스객체 (list tuple,문자열):
  반복할 코드
```

### **for문을 이용하여 1-100까지 숫자 출력**

```python
for i in range(1,101):
  print(i,end=' ')
1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92 93 94 95 96 97 98 99 100
```

```python
sum = 0 

for i in range(1,101):
  sum+= i 
print(sum)
```

---

### 입력한 횟수 만큼 반복하기

```python
count = int(input('반복할 횟수 입력 >> '))

for i in range(count):
  print(f'{i+1}번째 출력')
```

---

### 시퀀스 객체로 반복

• 여러가지 자료가 연속적으로 들어있는 , list,tuple,문자열 같은 시퀀스 객체를 for문에 사용하면 데이터를 한 개씩 꺼내오며 반복문이 실행된다.

```python
a = list(range(10,101,10))
a
for i in a:
  print(i,end=' ')
10 20 30 40 50 60 70 80 90 100
for i in 'Hello, Python':
  print(i,end=' ')
```

### 역순으로 꺼내오기 reversed()

```python
for i in reversed('python loop'):
  print(i,end=' ')

for i in 'python loop'[::-1]:
  print(i)

## 슬라이싱으로도 가능
```

### 🧈while문

- 반복할 횟수가 정해지지 않은 경우

```python
# 초기화 변수 선언 필수 
while 조건식 : 
#반복할 코드
```

---

### **while문을 사용해서 1-100까지 더하기**

```python
i = 1 
result = 0 

while i <= 100 :
  result += i 
  print(result,end=' ')
  i += 1
```

```python
i = 100 
result = 0 

while i >= 1 :
  result += i 
  i -= 1
print(result)
```

역순 정순 같이 

---

### **반복 횟수가 정해지지 않은 경우 while True**

무한반복

### **True가 되는 경우 : 1 ,정수 ,실수, 문자열, True**

### **False가 되는 경우 : 0 false , none, 0.0, '' ,[],(),{}**

### **countinue로 코드 실행 건너뛰기**

```python
i = 1 
while True :
  if i > 100 :
    break 
  print(i)
  i += 1
```

```python
for i in range(100):
  if i % 2 == 0 :
    print(i,'짝수라서 숫자 인쇄 하지 않고 위로 올라간다')
    print()
    continue
  else :
    print('홀수라서 숫자를 인쇄함',i)
  print('반복문 끝:',i)
  print()

36 짝수라서 숫자 인쇄 하지 않고 위로 올라간다

홀수라서 숫자를 인쇄함 37
반복문 끝: 37

38 짝수라서 숫자 인쇄 하지 않고 위로 올라간다

홀수라서 숫자를 인쇄함 39
반복문 끝: 39

40 짝수라서 숫자 인쇄 하지 않고 위로 올라간다

홀수라서 숫자를 인쇄함 41
반복문 끝: 41

42 짝수라서 숫자 인쇄 하지 않고 위로 올라간다

홀수라서 숫자를 인쇄함 43
반복문 끝: 43
....
```

## 🍕중첩 반복문

• 중첩 반복문은 for나 while문을 2번 이상 겹쳐서 사용하는 것

- 각 반복문의 블럭 위치를 확인 (들여쓰기)
- 중첩 반복문의 실행 순서는 안쪽부터 바깥쪽으로 실행된다.

---

## 🧈enmerate

인덱스와 자료를 한 번에 출력해주는 함수 enumerate(시퀀스객체(list,tuple,문자열))

------
## LIST 심화

## 1. **리스트와 함께 사용하는 함수**

- sorted() : 정렬
- min() : 최소값을 구해주는 함수
- max() : 최대값을 구해주는 함수
- sum() : 더해주는 함수

### 가장 큰 수 출력하기

```python
#원래는 max()함수 
a = [38,21,53,62,19]
max(a)
```

### search 함수 구현

```python
a = [38,21,53,62,19]

temp = a[0] 
for i in a :
	if temp <= i :
	temp = i 
	print(temp)
38
53
62

#알고리즘의 초석이 되는 비교란
```

### **LIST 표현식 (list comprehension) 사용하기**

- list 안에 for 반복문과 if else 조건식을 한번에 적용
- 다소 복잡해 보일 수 있으나, 여러 줄의 코드를 1줄로 줄일 수 있고, for,if else문을 쓸 때 보다 처리 속도가 빠릅니다.

`[식 for 변수 in list]`

```python
# 0부터 9까지 숫자를 생성하여 리스트 생성 
[x for x in range(1,10)]
[1, 2, 3, 4, 5, 6, 7, 8, 9]

[x for x in range(1,10) if x%2 ==0]
[2, 4, 6, 8]
```

---

## **파일 읽기, 파일 쓰기**

- open()
- with open()

**1) open()**

- 파일에 문자열을 쓰거나 읽을 때는 open 함수로 파일을 열어서 write 메소드를 사용해 저장

```python
변수명 = open("파일이름",파일모드(w,r,bw,br)
변수명.write("저장할 내용")
변수명.close()
```

close로 꼭 파일을 닫아 주어야함

**만든 파일 읽어오기 옵션만 w => r**

```python

변수1 = open("읽어올 파일명", 'r')
변수2 = 변수1.read()
변수1.close()
```

```python
file = open('test.txt','w')
file.write('파일 만들기 연습입니다.')
file.close()
```

with문 이용 

```python
with open('test_with.text','w') as file3:
  file3.write("파일 만들기 연습2")

with open('test_with.text','r') as file4:
  my_file2 = file4.read()

print(my_file2)
```

## 🍜실전 예제

- **readlines() : 파일을 한 줄 씩 읽어와서 list로 변경**

[hotels.com](http://hotels.com)에서 크롤링한 데이터들을 읽어온다. 

```python
with open('/content/drive/MyDrive/hotels_info.csv', 'r' ) as test_file:
  my_read_file = test_file.readlines()

print(my_read_file)
```

```python
hotelId,hotelName,tripType,tripTypeText,reviewDate,rating,description,isKorNot\n',
 '356,105343,서울 웨스틴조선호텔 (The Westin Chosun Seoul),family,1박 가족 여행,2019년 1월 26일,10.0,직원들 서비스나 마인드 완벽합니다 다만 노후된 시설과 좁은 라운지가 호텔 이름에 비해 약간 부족합니다,True\n',
 '357,105343,서울 웨스틴조선호텔 (The Westin Chosun Seoul),family,1박 가족 여행,2019년 2월 4일,10.0,웨스틴조
```

대략 이런식으로 나와있다

list 형식으로 바뀌었는데 이걸 리뷰만 긁어오고싶다~ 

그럼 어떻게 해야하느냐? 

for문을 이용하면 리스트가 풀리는데 이 부분을 split을 이용해서 콤마로 나누어 주고 / 그 안에서 다시 잡힌 리스트 내에서 추출해주고 싶은 인덱스를 반복해서 추출해주면 된다.

Detail Logic

사용자 리뷰 - 호텔이름, 여행종류, 평점,리뷰글.split(’,’)

```python
all_reviews = []
for reviews in data:
	temp = review.split(’,’) - 호텔 정보가 담긴 list 
	temp2 = temp[7] 
	all_reviews.append(temp2)
```

---

### JSON 언패킹

## **서울특별시 관광지 입장정보 JSON 데이터 언패킹하기**

```python
with open ('/content/drive/MyDrive/서울특별시_관광지입장정보_2011_2016.json','r') as file :
  dict_list = file.read()
```

```python
tour_info = []

for i in dict_list:
  for_num = i.get('ForNum',0)
  gun_name = i.get('gungu','unknown')
  res_num = i.get('resNm',0 )
  acd_num = i.get('addrCd',0)
  r_num = i.get('rnum')
  sido_name=i.get('sido','unknown')
  day_num = i.get('yyyymm',0)
  Nat_num = i.get('NatNum',0)

  tour_info.append([for_num,gun_name,res_num,acd_num,r_num,sido_name,day_num,Nat_num])
```

for문으로 돌면서~ get을 넣어준다 만약 get을해서 없으면 0을 반환하고 있으면 값을 가져와주는 함수 

### 대략적으로 아이템들이 모여진걸 확인할 수 있다.

그것을 다시 딕셔너리로 묶어주려면

```python
tour_info2= [] 
#for_num,gun_name,res_num,acd_num,r_num,sido_name,day_num,Nat_num

for i in tour_info:
  create_dict = dict(외국인수=i[0],시군구명=i[1],관광지명=i[2],관리번호=i[3],관리번호2=[4],시도명=i[5],일자=i[6],나라번호=i[7])
  
  tour_info.append({for_num,gun_name,res_num,acd_num,r_num,sido_name,day_num,Nat_num})
	tour_info2.append(create_dict)
```

완성이다 

오늘 내용 요약하자면 리스트 연산함수 / 읽기 쓰기 with문 / 리스트 컴프리헨션 / 딕셔너리 언패킹 패킹 등이다.

-----

# 함수

## 1.함수(function) 사용하기

- 자주 사용할 기능을 미리 만들어서 반복 재사용 할 수 있게 만든 것
- print(),split(),input() 등은 미리 만들어놓은 함수이다.

```python
def function():
  code...
  return
```

```python
# hello 파이썬이라는 글자를 출력하는 함수 

def hello():
  print('python')
```

### 함수 호출 순서

```python
hello2()

def hello2():
  print('Hello2 function')

# 실행이 안된다 정의를 먼저 하고 나서 실행을 해야 한다. 
```

## **3) 함수의 매개변수**

- 함수의 매개변수는 함수명 뒤의 괄호 안에 넣는 변수

```python
def function(args):
  .... code
```

```python
def circle(c):
  return c * c * 3.14
circle(3)
28.26
```

### **4) 매개변수 2개짜리 함수**

덧셈 함수 만들기

```python
def calc(a,b):
  result = a + b 
  return result
```

```python
# 반환 값이 없는 경우 

def add(num1):
  total = num1 + 1
```

### **6) 함수에서 결과 값을 여러 개 반환하기**

```python
def function(args):
  ___ return result1, result2
```

- 기본적으로 함수에서 반환 하는 값은 1개임
- 2개 이상인 경우에는 튜플로 만들어서 반환 함

```python
def add_sub(a,b):
  return a + b , a * b
```

### **7) 중간에 함수를 종료시키기 위한 용도로 쓰는 return 이 있다 .**

```python
# 1-100까지 짝수만 출력하다가 51번째에 종료되게 하기 

def calc(age):
  for i in age:
    if i % 2 == 0 :
      print(i,end=' ')
    elif i == 51:
      return
```

```python
age = range(1,101)

calc(age)
2 4 6 8 10 12 14 16 18 20 22 24 26 28 30 32 34 36 38 40 42 44 46 48 50
```

### **2. 함수에서 위치 인수와 키워드 인수 사용하기**

1) 위치인수(positional argument)

- 함수에 인수를 순서대로 넣는 방식
- 인수의 위치가 정해져있다.

```python
def print_nums(a,b,c):
  print(a)
  print(b)
  print(c)
```

```python
print_nums(3,4,5)
3
4
5
```

### **2) 언패킹을 이용하여 언박싱 리스트 자료 차례대로 넣기**

- (에스트리크)를 list /tuple 앞에 붙여서 언패킹
- 단, 함수의 매개 변수와 리스트 / 튜플 요소 개수가 같아야 한다.

```python
L = [5,6,7]

print_nums(*L)
5
6
7
```

## **3) 가변인수**

- 여러 개의 자료 입력 받기 * args

```python
def sum2(*args):
  # args arguments의 약자
  hap = 0
  # args에서 변수 값을 받으면 초기 값은 무조건 튜플로 변환된다
  for i in args:
    hap += i
  return hap

sum2(1,2,3,4,5,6,7,8,9,10)
55
```

```python
L = [5,6,7]
sum2(*L)
18
```

## **4) 고정인수와 가변인수를 함께 사용하기**

- 고정인수와 가변인수를 함께 사용할 때는 고정 매개변수를 먼저 지정하고 , 그 다음 매개변수에 *을 붙여준다.

```python

def func(a,*args): # 고정인수,가변인수

def func2(*args,a) : # 가변인수, 고정인수 X 사용할 수 없음
```

- 고정인수가 오고 난 뒤에 가변인수가 들어가야 실행이 된다.

```python
# 1부터 10까지 숫자에 3을 곱하는 함수

def func(a,*args):
  result = []
  for i in args:
    print(a*i)
    result.append(a*i)
  return result

calc = func(2,*[1,2,3,4,5,6,7,8,9,10])
print(calc)

2
4
6
8
10
12
14
16
18
20
[2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```

## **함수 내에서 리스트 표현식 사용하기**

```python
def muls(a,*args):
  return [a * num for num in args]

muls(3,*[1,2,3,4,5,6,7,8,9,10])
[3, 6, 9, 12, 15, 18, 21, 24, 27, 30]
```

## **개인정보를 출력하는 함수**

```python
def personal_info(name,age,address):
  print(f'이름: {name}')
  print(f'나이: {age}')
  print(f'주소: {address}')

personal_info('홍길동',24,'서초구')

이름: 홍길동
나이: 24
주소: 서초구
```

## **위의 함수는 인수의 순서를 모두 기억 해야 하기 때문에 사용 하기 어려움**

- 인수의 순서와 용도를 매번 기억하기 않도록 하기 위해서 키워드 인수 (keyword argument)를 사용
- 예) print(a,sep='',end='n)에서 sep=과, end= 이 키워드 인수

```python
# personal_info 함수를 키워드 인수 방식으로 호출해보기

personal_info(name='홍길동',age=30,address='서초구 잠원동')
```

```python
# 키워드 인수 방식으로 호출할 경우 인수의 순서나 위치를 변경할 수 있다

personal_info(address='서초구 잠원동',name='홍길동',age=30)
```

## **5) 키워드 인수와 딕셔너리 언패킹 사용하기**

- *dict
- 함수의 넣는 인자를 딕셔너리로 넣을 때 사용
- 사용하는 방법은 **dictionary

```python
x = {'name':'홍길동','age':23,'address':'거어드레스불러보소'}
personal_info(**x)
이름: 홍길동
나이: 23
주소: 거어드레스불러보소
```

## **여러개의 값을 받아 매개변수 이름과 값을 출력하는 함수**

```python
def personal_info2(**kwargs): #kwargs(keyword arguments)
  print(kwargs)
  print(type(kwargs))
  for kw,arg in kwargs.items():
    print(kw,':',arg,sep='')

y = {'주소':'마 어드레스 부르소'}

# 인수를 한개만 입력
personal_info2(name='홍길동')
name:홍길동
```

```python
# 인수를 한개만 입력
personal_info2(name='홍길동',address='마 어드레스 부르소',age=30)

#{'name': '홍길동', 'address': '마 어드레스 부르소', 'age': 30}
#<class 'dict'>
#name:홍길동
#address:마 어드레스 부르소
#age:30

# print문으로 kwargs, type kw,args를 모두 출력하라고 지시했기 때문에 다같이 출력됨

```

---

## *kwargs를 사용한 가변 인수 함수 코딩

- 딕셔너리 형태의 자료가 들어오므로 함수 내에서 key가 있는지 확인하는 코드가 필요

```python
def personal_info3(**kwargs):
  if 'name' in kwargs:
    print(f'이름 : {kwargs["name"]}')
  if 'age' in kwargs:
    print(f'나이 : {kwargs["age"]}')
  if 'address' in kwargs:
    print(f'주소 : {kwargs["address"]}')

personal_info3(**x)
이름 : 홍길동
나이 : 23
주소 : 거어드레스불러보소
```

## **6) 위치 인수와 키워드 인수 함께 사용하기**

- 항상 위치 인수가 앞 쪽 키워드에 와야 함

```python
def func(위치인수,키워드인수):
def func(*가변인수,**키워드인수):
```

```python
def custom_print(*args,**kwargs):
  print(*args,**kwargs)
custom_print(1,2,3,'python',sep=':',end='')
1:2:3:python
```

## **3. 매개변수의 초기 값 지정하기**

- 함수를 호출할 때 인수의 값을 넣지 않고 생략 하고 싶을 때 사용
- 예) print문 사용할 때 sep는 기본 값이 공백 → " " end는 기본 값이 _\n 인데 매번 지정하여 넣지 않아도 기본적으로 입력 되어 작동함.

```python
def personal_info4(name,age,address='비공개'):  #address는 기본값을 '' 공백을 default로 둠
  print(f'이름 : {name}')
  print(f'나이 : {age}')
  print(f'주소 : {address}')

personal_info4('홍길동',24)
이름 : 홍길동
나이 : 24
주소 : 비공개

personal_info4('홍길동',24,'서초구') #값을 넣어주면 default 값인 비공개가 없어지고 서초구가 출력이 된다
이름 : 홍길동
나이 : 24
주소 : 서초구
```

## **초기 값이 지정된 매개변수의 위치는 반드시 가장 마지막어야 함.**

```python
def personal_info4(name,address='비공개',age):  #address는 기본값을 '' 공백을 default로 둠
  print(f'이름 : {name}')
  print(f'나이 : {age}')
  print(f'주소 : {address}')

File "<ipython-input-97-7a36956e9ff5>", line 1
    def personal_info4(name,address='비공개',age):  #address는 기본값을 '' 공백을 default로 둠
                                          ^
SyntaxError: non-default argument follows default argument
```

## **default 값은 가장 마지막에 배정하지 않으면 상기 오류가 나타난다.**

- non-default argument follows default argument

---

## 두 수의 사칙연산 계산기 만들기

```python
def calc2(a,b):
  print(f'{a} + {b} = {a+b}')
  print(f'{a} - {b} = {a-b}')
  print(f'{a} * {b} = {a*b}')
  print(f'{a} / {b} = {a/b}')

calc2(5,3)
```

## **입력된 문자가 한글인지 판별하는 함수**

- ord() 문자 1개를 아스키 코드 값으로 변환, 한글의 아스키코드 범위는 12593-55203까지

문자를 입력 받아 한글인지 아닌지 판별하는 함수를 작성하시오

```python
# 풀이

def is_ko(ch):
  start = 12593
  end = 55203
  if start<= ord(ch)<= end :
    print('한글')
    return True
  else:
    print('한글이 아닙니다')
    return False

# user_input = input('문자열을 입력하세요 >> ')
is_ko('')
```

다른버전 

```python
def kor_is(ch):
  for i in ch:
    ascii = ord(i)
    if 65 <= ascii <= 122:
      return '영문자'
    elif 12593 <= ascii <= 55203:
      return '한글'
    else:
      return '범위 이외의 글자입니다'

user_input = input('입력 >> ')
kor_is(user_input)
```

- 참고 : ord 함수는 특정 문자를 유니코드 번호로 바꾸어주는 함수이다

---

## **4. 함수 Doc 스트링 사용하기**

- 함수의 기능을 설명하거나, 사용법을 함수 내에 적어 놓는 것

```python
def func(매개변수):
  ____ """DocStr('함수에 대한 설명')"""
  __ code

  - return

```

- 독스트링은 함수 실행시에는 출력되지 않는다.
- 독스트링을 출력 하고 싶을 때에
    - print(함수이름.**doc**)
    - help(함수이름)이 2가지 방법으로 출력한다

---

## **실습**

add 함수에 doc 스트링 입력하여 실행 및 출력해보기

```python
def add(a,b):
  """
  이 함수는 a와 b를 더한 뒤 결과를 반환하는 함수입니다.
  """
  return a + b

Help on function add in module __main__:

add(a, b)
    이 함수는 a와 b를 더한 뒤 결과를 반환하는 함수입니다.

None
```

---

# **람다 표현식(lambda expression)**

- 함수 이름이 없는 함수 (익명함수)
- 간단한 함수 작성 하거나 다른 함수의 인수로, 함수를 넣을 때 사용한다.

```python
# 10을 더하는 함수 기존 
def func(x):
  return x + 10
func(5)

15
```

## **람다함수를 만든 뒤 호출하기**

```python
# 10을 더하는 함수 

(lambda x: x+10)(5)
```

## **람다 함수를 변수에 넣고 변수에 인수를 넣어 호출하기**

```python
plus_five = (lambda x : x+5)
plus_five(5)

10
```

## **람다 표현식을 함수의 인수로 사용하기**

```python
def plus_ten(x):
  return x + 10

list(map(plus_ten,[1,2,3])) #맵으로 1,2,3을 매핑해서 함수에 넣어준 후에 , 리스트로 반환 시켜줌

[11, 12, 13]

list(map(lambda x : x + 10,[1,2,3])) #람다로 축약
[11, 12, 13]
# 결과가 같다
```

## **람다 표현식의 조건부 표현식 사용하기**

- 리스트 컴프리헨션을 이용하여 사용한다.

```python
# 3의 배수만 문자열로 바꾸기 

result = []

def three(*args):
  for i in args:

    if i % 3 == 0 :
      i = str(i)
      result.append(i)
    else: 
      result.append(i)
  return result

a = three(*[1,2,3,4,5,6,7,8,9,10])

print(a)
[1, 2, '3', 4, 5, '6', 7, 8, '9', 10]
```

### 3의 배수만 문자열로 바꾸기

```python
L = [1,2,3,4,5,6,7,8,9,10]

list(map(lambda x: str(x) if x % 3 == 0 else x,L))
[1, 2, '3', 4, 5, '6', 7, 8, '9', 10]
```

### map 함수에 표현식을 넣어 여러개의 리스트 연산하기

```python
a = [1,2,3,4,5]
b = [2,4,6,8,10]
c = [3,6,9,12,15]

list(map(lambda x,y,z: x * y * z,a,b,c))
[6, 48, 162, 384, 750]
```

### **filter 함수를 사용하여 조건에 맞는 요소만 가져오기**

```python
def f(x):
  return 5 < x < 10

a = [8, 3, 2, 10, 15, 7, 1, 9, 0, 11]

list(filter(f,a)) #5보다 크고 10보다 작은 수만 출력
[8, 7, 9]

list(filter(lambda x: 5<x<10,a)) # 상기 함수와 같은 식을 lambd로 사용 하기
[8, 7, 9]
```

### **find 함수 사용하여 이미지 파일만 가져오기**

- find('찾을 내용') → 찾을 내용과 일치하는 문자열에 시작 인덱스를 반환 하고, 없을 시 -1을 반환한다.

```python
files = ['font','1.png','10.jpg','11.gif','2.jpg','3.png','table.xlsx','spec.doc']

for idx,i in enumerate(files):
  if i.find('.png') != -1:
    print(f"{idx+1}번 {i} : {i.find('.png')}")
2번 1.png : 1
6번 3.png : 1

list(filter(lambda x: x.find('.png') != -1 or x.find('.jpg') != -1,files))

['1.png', '10.jpg', '2.jpg', '3.png']
```
