# Python

### 자료의 타입

- int = 정수형 

  - %d 

    `'%d %d' % (1,2)`

    `%d` 자리에 1과 2가 들어감

- float = 실수형

  - %f

    `'%f' % 3.14`

    `%f` 자리에 3.14가 들어감

- str = 문자열

  `"String"  'String'  `

  값을 변경할수없고 순서를 변경할수없다

  `"""  ''' `3개씩하면 줄바꿈에도 한꺼번에 저장

  - %s

    `'My name is %s' % 'Young Choi'`

    퍼센트 뒷부분 문자열이` %s` 로 들어감

  - indexing

    원하는 값의 하나만 빼옴

    `my_name = "김왼손"`

    `my_name[2]` 하면 '손' 값이 출력

    `my_name[-1]`해도 '손' 값이 출력

  - slicing

    원하는 값을 어려개를 지정해서 출력

    `my_name = "김왼손 왼팔"`

    `my_name =[1:4]` '왼손 ' 값이 출력

    `my_name =[:3]` '김왼손' 값이 출력

    `my_name =[4:]` '왼팔' 값이 출력

    - .split() 

      문자열을 공백단위로 잘라서 저장

      `my_name = "김왼손 왼팔"`

      `my_name.split()` '김왼손','왼팔' 값이 출력

    - Docstring

      """를 자체로 주석으로 사용

    - end, 이스케이프 코드

      `print('집단지성', and = '')` and는 출력의 끝에 추가로 출력할 수있다.

      `\n \t` 도 넣을수 있다.

      

- 

### 리스트, 튜플 딕셔너리

- **list**

  [] 대괄호 사용 , 여러개의 값을 한꺼번에 모아서 저장

  - 리스트 메서드

    - .insert()

      `my_list.insert('앞에값추가')`

    - -.append()
      `my_list.append('뒤에값추가')`

    - .pop() , del

      `my_list.pop()` 리스트 뒤의 값 제거

      pop(0) 를 입력하면 앞의 값이 제거됨

      `del my_list[0]` 0번자리에 있는 값을 제거

    - .sort()

      `my_list.sort()`가나다 순으로 리스트 정렬

    - .count()

      `my_list.count('바다소')` '바다소' 값의 갯수를 출력

  - 인덱싱, 슬라이싱을 할수 있다.

- **Tuple**

  ()  소괄호 사용, 값을 바꿀수없음, 소괄호를 사용하지않아도 튜플이됨

  - packing

    `my_ tuple = 1,2,3`

    `num1, num2, num3 = my_tuple` 입력하면

    각각 `num1 = 1, num2 = 2 num3 = 3` 가 됨

  - unpacking

    `num1 ,num2 = num2, num1` 을하면

    `num1 = 2 , num2 = 1 `이됨

- **Dictionary**

  `{key1:값, key2: 값}` 키와 값을 지정
  
  비어있는 `my_dict[0] = 'a'` 을하면 `my_dict = {0:'a'}` 가 추가됨
  
  `my_dict[0]` 을 하면 `'a'`가 출력
  
  list와 같이 `del my_dict[0] ` 키값을 입력하면 삭제
  
  - .values()
  
    `my_dict` 의 값만 가져옴
  
  - .keys()
  
    `my_dict`의 키만 뽑아옴
  
  - .items()
  
    `my_dict` 의 키와 값을 뽑아옴
  
  `for std in my_dict.keys() :`
  
  `print(std)`
  
  이와 같이 사용

### 주석

- '#' 뒤에있는 문자를 주석으로 처리


### 함수

대소문자를 엄격하게 구분

내장 함수, 모듈의 함수, 사용자 정의 함수 가있다.

모듈의 함수 = inport를 해서 가져다 쓸수있는 함수

사용자 정의 함수  = 사용자가 직접만드는 함수

- 사용자 정의 함수

  `def 함수이름(인자1,인자2,...)`

  `실행할 명령1`

  `    실행할 명령2`

  `return 결과`

  - `def add(num1,num2):`

    `return num1 + num2`

    다음 `add(1,2)` 하면 `3`이 출력된다

  - 언패킹 사용가능, 여러개 사용가능

- print() =출력

- input() = 입력

- Boolean 

  `True` or `False` 를 알려줌

- '{ }'.format()

  'My name is  {}'.format('조희진')

  {} 자리에 조희진이 들어감

  `'{} * {} = {}'.format(2,3, 2*3)`

  `'{1} * {0} = {3}'.format(2,3, 2*3)`

  {} 안의 숫자는 포맷의 자리

- len()

  `len(my_list)` 리스트의 값의 갯수를 세줌

- type()

  함수의 타입을 알수있음

### 연산자

- assign(할당연산자)

  = , += , -=,*=,/=

- arithmetic(산술연산자)

  +, - , *, /

  **(제곱), //(나누기몱), %(나누기나머지) 

- %로 홀짝 구분

  홀수만 출력하기

  `for i in range(100):`

  ​	`if i%2 ==1`

  ​		`print(i)`

- 문자열 연산자

  +, * 

- 비교연산자

  ==, !=, > , < , >=, <=

- 논리연산자

  and ||, or&&, not 

- 멤버쉽

  리스트같은 곳에 값이 있는지 없는지 확인

  in, not in

  `'찾은것' in list`  있으면 true 없으면 false 로 출력됨

### for 문

`or 변수 in 컨테이너 :`

​    `실행할명령1`

​    `실행할 명령2`

- range()

  `range(3)` 은 `[0,1,2]` 가 출력됨

- for * 2

  - 구구단 만들기

     `for n in range(1,10):`

    ​	``for i in range(1,10):`

    ​		`print('{}*[]={}'.format(n,i,n*i))`

- 컴프리헨션

  `:`를 사용하지않고 한줄로 코드를 작성 

### if문

조건이 참인지 거짓인지 판단 

`if 조건 :`

​    `실행할 명령1`

​    `실행할 명령2`

- if

  `name = '김왼손'`

  `if name == '김왼손'`

  `print('만나서 반가워요',name)`

  `만나서 반가워요 김왼손`이 출력됨

- else

  조건문이 false일때 출력할 명령을 입력

- elif 

  if 문에 또다른 if문을 사용할때 elif를 쓴다

### while문

조건이 참이면 계속 반복

`while 조건:`

​    `실행할 명령1`

​    `실행할 명령2`

- while

  `while count < 3:`

  ​    `print('횟수',count)`

  ​    `count +=1`

  `횟수1, 횟수2, 횟수3` 이 출력됨

- continue

  현재 명령을 실행하지않고 조건으로 되돌아감

- break

  현재 명령을 중단시킴

### 모듈 

비슷한 함수들을 모아논 파일 

자신만든것,  파이썬에서제공한것, 다른사람이 만든것 을 사용할수 있다

`import` 키워드 사용, 빠르게 개발이 가능하게 해준다

- random 모듈

  `import random` 랜덤 모듈을 불러온다

  `random.choice(list)` 을 할 경우

  list의 값하나가 랜덤으로 출력

  `random.sample(list,2)` list 의 값을 랜덤으로 2개 출력

  `random.randint(1,9)` 숫자의 범위를 지정 그안에 무작위숫자 하나를 출력

### 객체(Object)

현실의 사물, 물체, 물건을 컴퓨터에 구현한것, 함수와 데이터를 묶어서 만든것

파이썬에선 거의 모든것이 객체이다 (list, Tuple, int 등등) 구현한것

- 용사를 만든다하면 체력, 마나, 스테미나, 가능한행동 을 함수로 구현한것을 객체라 한다



### 코딩 스타일

파이썬 공식홈페이지에 PEP8 파일을 보면 코딩스타일에대한 정석이 나온다

영어가 어렵다면 구글에 번역판이 올라와있다



### 구글링 방법

모르는게 있으면 구글링을 할것