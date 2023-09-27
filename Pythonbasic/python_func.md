# python 함수
- `max( )`
- `random()`
    - import random으로 불러주기
- `random.randint(num,num)`              
    - 숫자사이에서 랜덤숫자 하나 출력
    - example 메뉴출력

    - menus = ('김밥', '라면', '만두')

      random_number = random.randint(0,2) 

      print(menus[random_number]) //  배열로


- `random.choice()`
    - 랜덤으로 글자 하나 받아온다
    - menu = random.choice(menus)

    print(menu)   //chocie함수

- `range(n,n)`: 숫자 범위설정
    - numbers = range(1, 46)

- `sample(  , n)`:어떠한 데이터프레임에서 랜덤하게 n개의 데이터(인덱스)를 뽑아야 할 때 사용
    - luchky number = random.sample(numbers, 6)
    //numbers에서 6개 받아온다.

- `sorted()`: 정렬 함수
    - 순서대로 정렬

 
- `requesets`: 파이썬으로 HTTP 통신이 필요한 프로그램을 작성할 때 사용
1. pip install requests//설치

2. import requests//불러옴

    URL = 'www. '

    res = requests.get(URL)

    data = res.json()
    //문자열 json형태로 변환












