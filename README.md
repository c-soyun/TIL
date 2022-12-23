# 2022.12.23 문제 풀면서 해결해나간 기록 

## 문제

### Problem A

인기 영화 조회 인기 영화의 개수를 출력합니다. 

1. `requests`를 이용하여 인기 영화 정보(Get Popular)에 요청을 보냅니다. 

2. popular를 기준으로 받아온 데이터에서 영화 리스트의 개수를 계산합니다.  

3. 계산한 정보를 반환하는 함수 `popular_count`를 완성합니다. 



  우선 처음에 requests 를 이용해서 
  
 import requests
   
key = '000'

url = 'https://=ko-KR'

이런식으로 키 값을 영화사이트에서 받고 

받은 키값으로 인기영화정보 클릭 -> 본인 키값 대입 -> url 획득 

그 다음 json 을 이용해서 

data = requests.get(url).json() 식을 써주면 1단계는 완성이다 

다음 2 번인  popular를 기준의 영화 리스트의 개수를 구하면되는데 

def popular_count():

    result = data['results']
    a = len(result)
    return a


def 를 사용했고 result 를 변수로 둔다음 1번에서 다운받았던 date인 results 를 대입시켜주고 

len 사용 해서 
return 을 돌려주면 끝!



마지막  print(popular_count())

해서 리스트의 갯수를 구해봤다

