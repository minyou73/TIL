# 미세먼지

- import requests 

    //  https 파일 불러오기

- from pprint import pprint  
    // 보기좋게 정리

- URL = 'http://apis.data.go.kr/B552584/ArpltnInforInqireSvc/getCtprvnRltmMesureDnsty?serviceKey=%2B58fRxySTvs0PfFQUY4WIxmfUdNzO2PRCGrFR%2BwurNXadOEb4nRyU4TfZFft%2FX7IOwZchblSbWUzs2S9mm1q2Q%3D%3D&returnType=json&numOfRows=100&pageNo=1&sidoName=%EC%84%9C%EC%9A%B8&ver=1.0'


- res = requests.get(URL) 
    // res에 url  저장

- data = res.json() 

    // url을 json 형태로

- items = data['response']['body']['items']

//directory 형식으로 구성된것중에서 response안에 body 안에 items 찾음

//list형태까지

>reuests.get(URL).json()['response']['body] // 이렇게 쓸수도 있다



- for item in items: // list형태(items) 안에 item 정의하여 '
    
- if item['stationName'] == '강남구': // 강남구 찾기

    print(item['pm10Value']) // 그중 pm10Value값 출력


        








