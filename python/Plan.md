## Plan



#### 2018 - 11 - 14 (스터디 1차)

- 함수에 대해 배우자.

  ```python
  def functionName(parameter1, parameter2):
      return parameter1+parameter2
  ```



  - def functionName(parameter):

- 2장 파이썬 프로그래밍 기초, 자료형

  - 숫자형

    - 정수/실수 차이 알기
    - 연산자 사용하기(각각의 함수로 만들 것.)
      - +(sum)
      - -(minus)
      - *(multiply)
      - **(pow)
      - /(divide)
      - //(int divide)

  - 문자열 -> immutable !

    - ''
    - " "
    - indexing
      - indexing 한 문자를 바꿔보자.
    - slicing
    - indexing / slicing 후의 값은 기존의 객체와 동일할까?
    - 깔끔한 출력해보기 - 고급 문자열 포매팅
      - "내 이름은 {number}이고 취미는 {hobby}야".format(number='마지환',hobby='게임')
      - %s
      - %d
      - %f
      - %c
    - 함수를 사용해보자
      - count
      - find vs index
      - join
      - upper
      - lower
      - lstrip
      - rstrip
      - strip
      - replace
      - split

  - 타입 확인하기

    - type
      - 왜 타입이 중요할까 ?
    - string->int
    - int->string

  - 리스트

    - 인덱싱
      - 수정해봐. 되나 안되나
    - 슬라이싱
      - a[1]=[1,2,3]
      - a[1:2]=[1,2,3]
    - +(리스트 더하기)
      - extend와 같다.
    - *(리스트 반복하기)
    - 요소 삭제하기 []
    - del 사용하여 요소 삭제하기
      - del a[1]
    - 동적으로 리스트에 요소 추가하기.
      - 동적의 의미 ?
        - a=[1,2,3]
        - a[3]=5 해봐.
      - a.append()
    - 리스트에서 특정 요소의 인덱스 찾기
      - list.index(value)
    - 리스트 중간에 특정 요소 넣ㅇ기
      - list.insert(0,4)
    - 리스트에서 특정 요소 제거하기
      - list.remove(index)
    - 제거 및 반환 -> append/pop을 이용하여 스택처럼 사용 가능.
      - list.pop() -> 맨뒤
      - list.pop(3) -> index 3번째놈.

  - 튜플

    - 배열과 똑같, but 변경 불가.

  - 딕셔너리

    - 존나 중요. key - value 형태로 저장이 가능. 후에 json이라는 파일 많이 ~ 볼텐데 그거랑 똑같음.
    - 잘쓰면 ㅈㄴ 빠름
    - 리스트로 구현한 wordcount vs Dictionary로 구현한 wordCount
    - 추가
      - map[key]=value
      - 덮어씌워질수도 있는데 ?
      - 
    - 삭제
      - del map[key]
    - 키값들 얻기
      - map.keys()
      - 얻어서 뭐함 ?
      - 키를 기억하지 않아도, 접근이 가능함.
    - 밸류만 얻기
      - map.values()
    - 둘다 얻기
      - map.items() -> 튜플로 돌려줌
    - 싹다 치우기
      - map.clear()
    - 키값으로 밸류값 얻기.
      - map.get(key)
      - 아니 map[key] 쓰면되지 이거 왜씀 ?
      - None 주거든. 
    - 키 있나 확인하기
      - key in a 이거 쓰지말고 그냥 None 쓰는게 나을듯. for i in range 랑 핵헷갈림

  - 집합

    - 생성 set([val1,val2,val3,..])

    - 음. value가 key 값인 dictionary

    - 따라서 중복 X

    - 순서도 X

    - 왜씁니까

      - 기능이 좋아요
      - 집합답게 교집합
        - s1&s2
        - s1.intersection(s2)
        - &는 혼동의 여지가 있음. 정석으로 아래꺼 쓰자
      - 집합답게 합집합
        - s1|s2
        - s1.union(s2)
      - 집합답게 차집합
        - s1-s2
        - s1.difference(s2)
      - 추가
        - s1.add(keyValue)
      - 여러개 펑펑 추가
        - s1.update([value1,value2,value3])
      - 특정 값 제거
        - s1.remove(value)

  - 자료형의 참 / 거짓

    - 거짓만 기억하자
    - 특징 : 없다. 비었따. 0이다 -> None이다
    - "" , [], (), {}, 0, None = False
    - 나머지 True 있으면 걍 다 True 완전 편하죠.

  - 자료형의 값을 저장하는 공간 변수

    - immutable vs mutable
      - 안변하고 (수정 안되고) , 변하고 (수정 가능하고)
      - 튜플이고, 리스트고
      - 문자열이고, 숫자고
      - 왜 파이썬에서 이렇게 immutable /mutable 엄격하게 해놨을까 
      - 아마 제 생각은 존나게 느린 언어여서 , 이거라도 실수하지 말라고 이래 해놓은거 같네요
    - == vs is 
      - 값이 같냐. 객체가 같냐
      - a=3 b=3 
      - a is b
      - a=[1,2,3]
      - b=a
      - b[2]=4
      - a is b 
      - 실수 갓
    - 리스트 복사
      - [:]
      - copy(list)

- 3장 프로그램의 구조를 쌓는다! 제어문

  - if문
    - 시각,촉각,청각,후각,미각
    - 파이썬만 있는거 이거 쓰자
      - in
      - not in
      - pass
        - ㅋㅋㅋ 그냥 조건을 걸지를 마세요
  - whille문
    - 그냥 존나게 끝까지 돌리고 싶을 때 씁니다.
    - 특정, 조건까지 돌리고싶을 때 써요
    - break
    - continue
    - pass vs continues
  - for문
    - 이게 가장 중요
    - range ? 암기 ㄴㄴ 이거 뭐냐
      - a=range(0,1000)
    - 야 이거 폴더 한개 파일 있거든 그거 전처리 해와
    - 야 이거 폴더 한개에 파일 100000개 있거든, 그거 내용은 똑같으니까 전처리 해와
      - for문 사용 ㄱㄱ
      - 폴더내부의 파일 이름을 list에 저장한다.
        - list 내부에서 파일 절대 경로를 읽어서 , 전처리를 한다.
    - 파이썬만의 문법
      - 리스트 안에 for 문 넣기.. 신기..
      - for문 + if문 넣기

- 4장 프로그램의 입력과 출력은 어떻게 해야 할까?
