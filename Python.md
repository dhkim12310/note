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

- list

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

- Tuple

  ()  소괄호 사용, 값을 바꿀수없음, 소괄호를 사용하지않아도 튜플이됨

  - packing

    `my_ tuple = 1,2,3`

    `num1, num2, num3 = my_tuple` 입력하면

    각각 `num1 = 1, num2 = 2 num3 = 3` 가 됨

  - unpacking

    `num1 ,num2 = num2, num1` 을하면

    `num1 = 2 , num2 = 1 `이됨

- Dictionary

  {key1:값, key2: 값} 키와 값을 지정
  
  비어있는 `my_dict[0] = 'a'` 을하면 `mydict = {0:'a'}` 가 됨
  
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

### 모듈

