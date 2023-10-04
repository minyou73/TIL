# 로또

> numbers = range(1, 46)


// 1~ 46까지 범위 설정

>lucky_number = random.sample(numbers, 6)

//luck_number에 numbers에 있는 6개의 값을 랜덤으로 입력


>print(sorted(lucky_number))

//숫자 정렬


>URL = 'https://www.dhlottery.co.kr/common.do?method=getLottoNumber&drwNo=1086'

- pip install requests //https      받아오는 함수 설치

> import requests

// 입력해야 사용 가능한 함수

>res = requests.get(URL)

//res에 https에서 가져온 url값 저장

>data = res.json()

//json 형태로

> drwtNo1 = data['drwtNo1']   
>drwtNo2 = data['drwtNo2']  
>drwtNo3 = data['drwtNo3']  
>drwtNo4 = data['drwtNo4']  
>drwtNo5 = data['drwtNo5']  
>drwtNo6 = data['drwtNo6']

//

>lotto_number = [drwtNo1, drwtNo2, drwtNo3, drwtNo4 ,drwtNo5, drwtNo6]

//받아온 값들 list형태로 lotto_number에 저장

>print(lucky_number)

//내가 임의로 뽑은 값 lucky_number 출력

>print(lotto_number)

//lotto_number 출력

>print(set(lucky_number) & set(lotto_number))

//lucky_number와 lotto_numer 비교해서 일치하는 값만 출력