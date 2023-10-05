# 1. 제어문
## 1.1 조건문(if문)

```python 
if<조건식>:  
    if의 조건식이 참인 경우 실행하는 코드
else:
    if의 조건식이 거짓인 경우 실행하는 코드
    

    1. 'if'문은 반드시 참/거짓을 판단 할수 있는 조건식과 함께 사용한다.
    2. '조건식'이 참인 경우 ':' 이후의 문장을 실행한다
    3. '조건식'이 거짓인 경우 : 'else:' 이후의 문장을 실행한다

    
```
## 1.2 elif
```python

if<조건식>:
    if 조건이 참인경우 실행
elif<조건식>:
    elif 조건이 참인 경우 실행
...    
else:
    위의 조건식에 하나도 부합하지 않는 경우 실행

```

## 1.3 조건표현식
> true_value if <조건식> else false_Value

# 2. 반복문
## 2.1 while문

```python
while <조건식>:
    실행할 코드
```
```python
a = 0

while a < 5:
    print(a)
    a += 1  # a = a +1
```
0   
1    
2  
3  
4  

## 2.2 for문
```python
for variable in sequence: 
    실행할코드
```
정해진 범위 내의 반복

```python
numbers = [1, 2, 3, 4, 5]
for number in numbers:
    print(number)
```
1  
2  
3  
4  
5
```python
numbers = range(31)

for number in numbers:
    if number % 2 == 1:
        print(number)

```
1  
3  
5  
7  
9  
11  
13  
15  
17  
19  
21  
23  
25  
27  
29  

```python
 # 리스트로 출력

numbers = range(31)
result = []

for number in numbers:
    if number % 2 == 1:
        result.append(number)
print(result)
```
[1, 3, 5, 7, 9, 11,13, 15, 17, 19, 21, 23, 25, 27, 29]

`append()` : 인자 추가

```python
for i in range(len(menus)):
    print(menus[i])
```
라면  
김밥  
떡볶이  
돈까스  

```python
for item in enumerate(menus):
    print(item)
```
`enumerate` : 튜플 형태로 만들어준다

## 2.3 dictionary 반복

1. for key in dict:
2. for key  in dict, keys():
3. for value in dict.values():
4. for key, value in dict.items():

```python
blood_type = {
    'A': 5,
    'B': 4,
    'O': 2,
    'AB': 3
```
```python
print('혈액형 목록은 다음과 같습니다')
for key in blood_type.keys():
    print(key)
```
A  
B  
O  
AB  
`key 값 단독으로 빼내기`
```python
for value in blood_type.values():
    print(value)
```
5  
4  
2  
3  
`value값 단독으로 빼내기`

```python
blood_type.items()
```
('A', 5)  
('B', 4)  
('O', 2)  
('AB', 3)  
`key:value 값 쌍으로 빼내기`

## 2.4 break
반복문을 종료시키는 키워드

## 2.5 continue
continue 이후의 코드를 실행하지 않고 다음 반복문을 실행
(다음 for문으로 진행)

## 2.6 else
else문은 끝까지 반복이 진행된 후 실행함(break을 만나지 않은 경우)
```python
numbers = [1, 2, 3, 4, 5]
target = 1

for n in numbers:
    if n == target:
        print('True')
        break
else:
    print('False')
```
True

## 2.7 pass
```python
if True:
    pass
```

## 2.8 match
```python
match value:
    case 조건:
        실행할코드
    case 조건:
        실행할 코드
    case _ :
        실행할 코드
```