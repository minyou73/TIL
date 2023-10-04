# Intro
## 1. 변수
>변수이름 = 값

- 변수이름은 어떤 이름이든 상관 없음  
- 영어, 숫자, _ 이용해 선언

## 1.1. number
- `int` = 1
- float = 1.1
- complex = 1-4j
- complex.imag = -4.0
- complex.real = 1.0

## 1.2. Boolean
- True
- False

## 1.3. None

## 1.4. String
> 문자열은 ', " 이용해 표현
- `'`hello`'`
- `"`hello`"`

> String interpolation
1. `% formating`
```python
print('홍길동은 %s살입니다.' % age)
```
2. `str.format()`
```python
print('홍길동은 {}살입니다.' .format(age))

```
3. `f-string`
```python
print(f'홍길동은 {age}살입니다.')

```

## 2. 연산자
## 2.1 산술 연산자
- a + b
- a - b
- a / b
- a * b
- a ** b (a=2, b=3 : a의 3제곱)

> 나눈 몫   
- a // b
> 나눈 나머지
- a % b
> mod
```python
print (divmod(a,b))
```
(0,2)

## 2.2 비교연산자
- a > b
- a < b
- a >= b
- a <= b
- a == b
- a != b

```python
print('hi' == 'hi')
print('Hi' == 'hi')

```
True   
False


## 2.3 논리연산자
- `and` : 양쪽 모두 True 일때 True 반환
- `or` : 양쪽 모두 False일때 False 반환
- `not` : 값을 반대로 반환

> True 1, False 0
```python
print(True and True)
print(True and False)
print(False and True)
print(False and False)

```
True   
False   
False   
False

```python
print(True or True)
print(True or False)
print(False or True)
print(False or False)

```
True  
True   
True  
False

```python
# 단축평가(and)
print(3 and 5)
print(3 and 0)
print(0 and 5)
print(0 and 0)
```

3  
3  
5  
0

```python
# 단축평가(or)
print(3 or 5)
print(3 or 0)
print(0 or 5)
print(0 or 0)

```
3  
3  
5  
0
## 2.4 복합연산자
- a += b (a = a + b)
- a -= b
- a *= b
- a /= b
- a //= b
- a %= b
- a **= b

## 2.5 기타연산자
```python
a = 'hi'
b = 'hello'

# concatenation
a + b = hihello
```


```python
a = [1, 2, 3]
b = [9, 8, 7]
a + b = [1,2,3,9,8,7]
```

```python
print(1 in [1, 2, 3])
print(100 in [1, 2, 3])

True
False
```

```python
a = 123123
b = 123123
print (a is b)

False   
# 저장되는 주소값이 다름
```
```python
a = 10
b = 10
print (a is b)

True
# -5 ~ 255 까지는 저장이 되어있음
```
> 연산자 우선순위
0. ()를 통해 그룹
1. **
2. 산술연산자(*,/)
3. 산술연산자(+,-)
4. 비교연산자 is, in
5. not
6. and, or

## 3. 형변환
## 3.1 암시적 형변환
```python
a = True
b = False
c = 1

print(a + c)
print(b + c)
```
2   
1

```python
int_num = 3
float_num = 3.3
complex_num = 3 + 3j

print(int_num + float_num)
print(int_num + complex_num)
```

6.3    
(6+3j)


## 3.2 명시적 형변환

 
```python
a = 1
b = '번'
a + b
```
- error

```python
print(str(a) + b)
```
- 1번

```python
a = '100'
print(type(int(a)))
```
- <class 'int'>

```python
age = input()
print(type(age))
```
- <class 'string'>

```python
age = int(input())
print(type(age))
```
- <class 'int'>


## 4. 시퀀스 자료형
- 시퀀스는 데이터의 순서대로 나열된 자료구조(순서대로 나열되어있다는 것은 정렬된것과는 다르다)

1. 리스트 (list)
2. 튜플 (tuple)
3. 레인지 (ragne)
4. 문자열 (string)

## 4.1 list(배열)
- 선언 : 변수이름 = [value1, value2, value3]
- 접근 : 변수이름[index]

```python
l = ['서울', '대전', '부산']

print(l[2]) = 부산

l[2] = '제주'
print(l[2]) = 제주
```

## 4.2 Tuple
- 선언 : 변수이름 = (value1, value2, value3)
- 접근 : 변수이름[index]
- list와 유사하지만 수정불가능
```python
x. y = (1, 2)
print(x, y)

x, y = (y, x)
print(x, y)
```
1  2  
2  1

## 4.3 range
- range(n): 0부터 n-1 까지 범위
- range(n,m): n부터 m-1까지 범위
- range(n , m ,s): n부터 m-1까지, +s만큼 증가

```python
r = (range(5, 15, 2))
print(r)
```
5 , 7, 9, 11, 13

## 4.4 string
> slicing
```python
mylist = [1, 2, 3, 4, 5]
mytuple = (11, 22, 33, 44, 55)
myrange = range(1, 10, 2)
```
```python
print(mylist[1:3])
print(mytuple[1:3])
print(myrange[1:3])
```
```python
print(mylist[1:4:2])
print(myrange[2:7:2])
```

## 5. 시퀀스데이터가 아닌 자료구조

## 5.1 set
- 수학에서 사용하는ㄴ 집합과 동일하게 처리(중복된 값이 없음)
- 선언 : 변수이름 = {value1, value2, value3}

```python
myseta = {1, 2, 3, 4, 5}
mysetb = {1, 3, 5, 7, 9}

print(myseta - mysetb)
# 차집합
print(myseta + mysetb)
#합집합
print(myseta & mysetb)
#교집합
```

## 5.2 dictionary
- 선언: 변수이름 = {key1:value1, key2:value2, key3:value3}
- 접근; 변수이름[key]
- key에는 immutable 한 모든 값을 사용가능
- value에는 모든 데이터가능

    - 시퀀스 자료형
    1. [list] : mutable
    2. (Tuple) : immutable
    3. range() : immutable
    4. 'string' : immutable

    - 시퀀스가 아닌 자료형
    1. {set} : mutable
    2. {dictionary}: mutable