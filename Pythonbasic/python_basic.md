# 1.저장 : 변수, variable
- 할당 assignment 오른쪽의 데이터를 왼쪽에 할당

- 1.`숫자 (int)`
 dust = 10
- 2.`문자 (string)`
dust = '5'
- 3.`참/거짓(boolean)`
dust = True #False

- print(dust)

# 2. 순서대로 적합 : list [ ]
`list[]`

dust_list = [10,20,0,50,100]



# 3. dictionary { } / key: value 

`dict { }`

dust_dict = {
    '서울': 100,
    '대전': 10,
    '부산': 50,
}

 print(dust_dict['부산'])

# 4. 조건 if

- `if`
- `elif`
- `else`

 age = 10
 if age > 20:
     print('성인입니다')
 elif age > 8:
     print('청소년입니다')
 else: 
     print('어린이입니다')



 dust 150보다 크다면 매우나쁨, 80~150 나쁨, 30~79 보통, 0~29 좋음

 dust = 200

 if dust >= 150:
     print('매우나쁨')
 elif dust >= 80:
     print('나쁨')
 elif dust >= 30:
     print('보통')
 else:
     print('좋음')


 if 150 <= dust:
     print('ㅁㅐ우나쁨')
 elif 80 <= dust <150:
     print('나쁨')
 elif 30<= dust and dust<80:
     print('보통')
 else:
     print('좋음')


# 5. 반복

`while`

menus = ['떡볶이', '피자', '스파게티', '김밥']

n = 0
- while n < 4 :
   
    print(menus[n])
    
     n=n+1

for menu in menus:
    print(menu)


