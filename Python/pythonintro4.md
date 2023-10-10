# 문자열 메소드
## (메소드==함수), 객체 안에들어있는건 메소드

```python
a = 'hello my name is minjung'   
#문자열은 immutable하기때문에 수정불가능
```

```python 
 a.capitalize()
print(a)
```
hello my name is minjung

```python
a = a.capitalize()
print(a)
```
Hello my name is minjung

- 원본에 있는 데이터는 변하지 않음, 함수는 실행후 return 반환, a는 유지
print(a)   


> `a.title()`  

'Hello My Name Is Minjung'

> `a.upper()`

'HELLO MY NAME IS MINJUNG'

> `join`
```python
my_list = ['hi', 'my', 'name']
''.join(my_list) 
'??'.join(my_list)
```


'hi??my??name'
-  ''기준으로 나눠서 my_list 들어가있는 요소 합쳐줌

>`.strip([chars]) `

```python
my_string = '        hello\n       '
print(my_string.strip())

```
hello
- 필요없는것 일괄처리    


> `replace(old, new[, count])  `
  
```python
a = 'wooooooooooooooooow'
a.replace('o', '!')
```
'w!!!!!!!!!!!!!!!!!w'


> `find(x)`
```python
a = 'apple'
print(a.find('p'))
print(a.find('z'))
```
1  
-1  
1


>`.index(x)`
```python
a = 'apple'
print(a.index('a'))
```
0

> `split(x)`
```python
a = 'my name is'
a.split()     

a = 'my_name_is'
a.split('_')  
```
['my', 'name', 'is']

-  쪼개고 리스트로 만들어줌 공백기준

> `.count(x)`
```python      
'woooooooooow'.count('o')
```
10
- 문자열 갯수 출력

# 리스트 메소드
```python
numbers = [1, 5, 2, 6, 2, 1]
```
> `.append(x)`
```python
numbers.append(10)
print(numbers)
```
[1, 5, 2, 6, 2, 1, 10]

> ` .extend(iterable)`

```python
a = [99, 100]

numbers.extend(a)
print(numbers)
```
[1, 5, 2, 6, 2, 1, 10, 99, 100]

>`.insert(idx, x)`
```python
numbers.insert(3, 3.5)
print(numbers)
```
[1, 5, 2, 3.5, 6, 2, 1, 10, 99, 100, 99, 100]

> `.remove(x)`
```python 
numbers.remove(3.5)
print(numbers)
```
[1, 5, 2, 6, 2, 1, 10, 99, 100, 99, 100]

> `pop()`
```python
numbers.pop()
print(numbers)

numbers.pop(0)
print(numbers)

numbers.pop()  
```

[5, 2, 6, 2, 1, 10, 99]  
[2, 6, 2, 1, 10, 99]  
99  #빠져나온 결과값 출력

> `sort()`
```python
numbers = [1, 6, 2, 1, 3, 2, 7 ,10]
print(numbers)
print(numbers.sort())  
 #결과값 none, 리스트가 바뀜
print(numbers)
numbers.sort(reverse = True)
print(numbers)

```
[1, 6, 2, 1, 3, 2, 7, 10]  
None  
[1, 1, 2, 2, 3, 6, 7, 10]  
[10, 7, 6, 3, 2, 2, 1, 1]  

> `sorted`
```python
numbers = [1, 6, 2, 1, 3, 2, 7 ,10]
print(numbers)
print(sorted(numbers))   
#원본은 그대로지만 바꾼거 출력, 정렬된값 return, python이 가지고 있는 함수
print(numbers)
```
[1, 6, 2, 1, 3, 2, 7, 10]
[1, 1, 2, 2, 3, 6, 7, 10]
[1, 6, 2, 1, 3, 2, 7, 10]

> `reverse()`
```python
numbers = [1, 6, 2, 1, 3, 2, 7 ,10]
print(numbers)

numbers.reverse()
print(numbers)

numbers = numbers[ : : -1]
print(numbers)
```
[1, 6, 2, 1, 3, 2, 7, 10]
[10, 7, 2, 3, 1, 2, 6, 1]
[1, 6, 2, 1, 3, 2, 7, 10]


## list comprehension
```python
# [1, 8, 27....1000] 세제곱 만들기
result = []

for number in numbers:
    result.append(number ** 3)
print(result)
```
```python
result2 = [ number ** 3 for number in numbers ]
print(result2)
```
[1, 8, 27, 64, 125, 216, 343, 512, 729, 1000]

# 딕셔너리 메소드
>  ` .pop(key[, default])`

>`update()`


>`get(key[, default])`


>

## dict comprehension
```python
dust = {
    '서울' : 100,
    '대구' : 30,
    '부산' : 50,
    '광주' : 80,
    '제주' : 20,
}
```

```python
result = {}
for k, v in dust.items():
    if v >= 50:
        result[k] = v
print(result2)
```
```python
result2 = {k:v for k,v in dust.items() if v >= 50}
print(result2)
```

# 세트 메소드
>`add(x)`

>`update()`

>`remove()`

>`pop()`

## map, filter, zip
> `map(function, iteable)`

>`filter`

>`zip`