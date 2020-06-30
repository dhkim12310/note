# Python repl.it

### Set

list와 마찬가지로 여러 다양한 타입의 요소들을 저장할수 있다

- List와 다르게 요소들이 순서대로 저장되어 있지 않습니다. 즉 ordering이 없다. 그러므로 for 문에서 읽어들일때 요소들이 순서대로 나오는게 아니라 무작위 순서대로 나옵니다.
- 순서가 없으므로 indexing도 없습니다. 몇번째 요소를 읽어들이거나 할 수 없습니다. 
- 동일한 값을 가지고 있는 요소가 1개 이상 존재 할 수 없습니다. 즉 중복된 값을 저장할 수 없습니다. 만일 새로 저장하려고 하는 요소와 동일한 값의 요소가 존재한다면 새로운 요소가 이 전 요소를 치환(replace)합니다.

```python
set = {1,2,3}
set2 = set([1,2,3])
```

두가지 방법으로 생성이 가능하다 set()함수를 이용할때 에는 list를 안에 넣어주어야 한다

set에서는 중복된값이 저장되지 않는다

list에서는 값을 추가하기 위해 append 메서드를 썼지만 set에서는 add라는 함수를 이용해야한다

```python
my_set = {1,2,3}
my_set.add(4)
```

삭제할때는 remove 함수를 사용하면 된다

```python
my_set.remove(1)
```

`'1'`값이 삭제된다

- **look up**

  set에서 어떤 값이 찾기위해 알아보는것을 look up 이라 한다

  set에서 특정값을 찾기위해서는 in 키워드를 사용하면 된다

```python
my_set = {1,2,3}

if 1 in my_set:
    print("1 is in the set")
> 1 is in the set
```

- **Intersection (교집합) & Union (합집합)**

  set은 교집합과 함집합을 구할때도 사용할 수 있다

  교집합은 **&** 키워드 혹은 **intersection** 함수를 사용하면 된다

  ```python
  set1 = {1, 2, 3, 4, 5, 6}
  set2 = {4, 5, 6, 7, 8, 9}
  ##교집합
  print(set1 & set2)
  > {4, 5, 6}
  
  print(set1.intersection(set2))
  > {4, 5, 6}
  ```

  합집합은 **|**키워드 혹은 **union** 함수를 사용하면 된다

  ```python
  print(set1 | set2)
  > {1, 2, 3, 4, 5, 6, 7, 8, 9}
  print(set1.union(set2))
  > {1, 2, 3, 4, 5, 6, 7, 8, 9}
  ```

  

-   get_unique_numbers_count 함수를 구현해주세요.

  get_unique_numbers_count 함수는 numbers 라는 parameter를 받습니다. 

  numbers는 list 입니다. Numbers의 고유 값들의 수를 리턴해주면 됩니다.

  예를 들어, 다음과 같은 input이 들어왔다면:

```python
[1, 2, 1, 1, 3, 4, 5]
```

5를 리턴해주면 됩니다.



```python
def get_unique_numbers_count(numbers):
  # 이 함수를 구현해주세요!
```

```python
return len(set(numbers))
```

> len() 함수는 저장되어있는 값의 숫자를 세는 함수, set()은 중복되는 값을 제거해주는 함수이다
>
> len(set()) 함수를 쓰면 중복되는 값을 제거하면서 갯수를 셀수 있다



### **Modules & Packages **

파이썬에서 모듈은 변수나 함수 그리고 클래스 등을 모아놓은 파일이다

- 다른파일에서 재사용 가능
- 전체코드가 한파일에 넣기에는 너무 커졋을때 여러 파일오 나누어서 정리를 하기 위해서

**모듈만들기**

단순히 파일을 만든후 그안에 자신이 원하는 함수, 클래스, 변수등을 구현하면 된다

그 후 다른파일에서 불러와 사용하면 된다 모듈을 불러오기 위해서는 `import` 키워드를 사용하면 된다 확장자 `.py`는 제외한다

```python
import <모듈 이름>
```

모듈을 import 한후 모듈의 원하는 변수/함수/클래스를 사용할 수 있다

```python
import <모듈 이름>.<모듈에서 사용하길 원하는 변수/함수/클래스 이름>
```

예를 들어, my_module 모듈의 my_module_func 함수를 호출하고 싶으면 다음 처럼 하면 된다

```python
my_module.my_module_func()
```

https://storage.googleapis.com/replit/images/1554632997345_f9021fb9b2e1ba5cc9af2f9182c16aec.pn

import 키워드 외에 from import 키워드를 사용해서 모듈을 불러올수 있다

```python
from <모듈 이름> import <함수/변수/클래스1>, <함수/변수/클래스2>, ..., <함수/변수/클래스N>
```

예를 들어, my_module 모듈에서 my_module_func 함수와 my_module_var 변수를 import 한다면 다음과 같다

```python
from my_module import my_module_func, my_module_var

print(my_module_var)
my_module_func()
```

import `*`를 사용하면 해당모듈의 모든 요소가 import 되지만 출동이 일어나기 쉽기 때문에 권장하지 않는다



**Import As**

여러 모듈의 import 하게  될 경우 출동을 방지 하거나 다른 모듈에서 동일한 이름의 함수가 있을경우 혹은, 모듈의 요소 이름이 너무 길경우 import as 키워드를 사용해서 새로운 이름을 주어서 사용할 수 있다

```python
from my_module  import my_func as f1
from my_module2 import my_func as f2
from my_module3 import function_with_name_too_long as f3

f1()
f2()
f3()
```

```python
import my_module as m1

m1.my_module_func()
```

모듈의 이름도 as를 사용 할 수있다



**packages**

모듈과 마찬가지로 다은 파일에서 불러와 사용한다, 모듈과 차이점은 모듈에 비해 더크고 복잡한 코드라는 점이다. 모듈은 단순한 파이썬 파일이지만 어떤 모듈들은 코드양이 너무 커서 한 파일에 다 넣기 비효율적일수 있다. 그럴경우 여러파일에 나누어서 코드를 관리하는게 효율적인데 이때 여러파일에 나누어져 있는 코드들이 다른곳에서 하나의 모듈로 불러와서 사용할 수 있도록 해주는것이 패키지이다

![](https://storage.googleapis.com/replit/images/1554634440159_dd22d36d0301f0b9d84188c0cbbe53d8.pn)

이런식 으로 모듈을 모아논 하나의 디렉토리를 패키지가 된다 

일반 모듈처럼 import하여 사용할 수 있다, 차이점은 클래스 객체를 사용할때 처럼 "dot notation" 으로 해당 package의 원하는 모듈을 import 해야한다

```python
import pkg.mod1
from pkg.mod2 import func2

pkg.mod1.func2()
func2()
```



가끔 package가 import 될때 초기 설정을 해줘야 할때가 있다

파이썬은` __init__.py`파일을 통해 package 초기 설정을 가능하게 해준다

 ![](https://storage.googleapis.com/replit/images/1554635895863_c805a2940ffe93d9e82fd8c2f6a0d813.pn)

package안에 `__init__.py`파일이 있으면 package가 import될때 자동으로 실행된다

`__init__`의 기능들이다

- import할떄 총 길이를 줄여주기
- Package에서 import 할 수 있는 변수/함수/클래스 제한하기

- package가 import될때 꼭 먼저 실행되어야 하는 코드들

**import 할때 총 길이를 줄여보자**

현재 pkg에서  mod1 의 func2 함수를 import하여 사용하기 위해서는 다음과 같이 해야한다

```python
import pkg.mod1

pkg.mod1.func2()
```

func2 함수를 호출할때마다 매번 모든 경로를 다 타입해줘야하기 때문에 번거롭다

함수 이름을 곧바로 호출 할수 있게 해보자

```python
# __init__.py
from .mod1 import func2
```

```python
# main.py
from pkg import func2

func2()
```

이렇게 `__init__`파일에 먼저 한번 import를 해주면 된다



 다음으로 `__init__`을 이용해 **변수/함수/클래스를 제한**해보자

예를 들어 모듈의 모든 함수가 다 외부로 노출될 수 있는건 아닐수 있습니다. 내부적으로만 사용되어야 하는 함수도 있을수 있다, 이러한 함수가 package 외부에서 import되어 사용되는 것을 막기 위해서는 __all__ 변수를 지정해 줄 수 있다

패키지를 통해 import 됭 수 있는 요소들은 모두 `__all__`변수를 통해 정의된다

그리고 `__all__`변수의 default 값은 모든 함수/변수/클래스 이다

따라서 `__all__`변수를 따로 정의해줌으로 import 될 수 있는 요소들을 제한 할 수있다

> `__all__` 변수는 string값의 요소를 가지고 있는 list 이다
>
> 따라서 import되길 원하는 요소들을 string으로 list에 선언해주면 된다

```python
# __init__.py
from .mod1 import func2
from .mod2 import func3

__all__ = ['func2', 'func3']
```

```python
# main.py
from pkg import *

func2()
func3()
func4() ## <== Error. func4 함수는 __all__ 에 정의되지 않았으므로 import 될 수 없음.
```



### **How import statement finds modules and packages**

파이썬이 module 과 package를 찾는 방법에 대해 알아보자

- import search 순서

  1. sys.modules

  2. built-in modules

  3. sys.path

**sys.modules**

파이썬이 모듈이나 package를 찾기위해 가장먼저 확인하는곳 이다.

sys.modules 는 단순한 dictionary이며 이미 import된 모듈과 package들을 저장하고 있다

즉 한번 import된 모듈과 package들은 파이썬이 또 다시 찾지 않아도 되도록하는 기능을 가지고 있다

**built-in modules**

파이썬에서 제공되는 공식 라이브러리들이다

**sys.path**

마지막으로 보는 장소가  sys.path이다

기본적으로 list이며 string 요소들을 가지고 있다

각 strong 요소들은 다음처럼 경로를 나타낸다

```
['',
 '/Users/song-eun-u/anaconda3/bin',
 '/Users/song-eun-u/anaconda3/lib/python36.zip',
 '/Users/song-eun-u/anaconda3/lib/python3.6',
 '/Users/song-eun-u/anaconda3/lib/python3.6/lib-dynload',
 '/Users/song-eun-u/anaconda3/lib/python3.6/site-packages',
 '/Users/song-eun-u/anaconda3/lib/python3.6/site-packages/aeosa',
 '/Users/song-eun-u/anaconda3/lib/python3.6/site-packages/IPython/extensions',
 '/Users/song-eun-u/.ipython']
```

파이썬은 각 경로를 하나하나 확인하면서 해당경로에 import 하고자 하는 package가 위치해 있는지 확인 한다

sys은 파이썬에 포함되어있는 모듈이며 다음처럼 sys모듈을 import해서 sys.modules와 sys.path 를 출력할수도 있고 수정할수도 있다

```python
import sys

print(sys.path)
print(sys.modules)
```

만약 sys에서도 모듈을 찾지 못하면 ModuleNotFoundError 에러를 리턴한다



### **Absolute Path & Relative Path**

- **absolute path**

  절대경로이다 import를 하는 파일이나 경로에 상관없이 항상 경로가 동일하다

  현재 속한 프로젝트 내에서는 어느파일, 위치에서 import를 해도 경로가 항상 동일하다

  전체적인 경로를 명시해주기 때문에 손쉽게 위치를 파악 할수 있으나 경로명이 길어지는 단점이 있다

- **Relative path**

  absolute path와는 다르게 프로젝트의 최상단 디텍토리를 기준으로 경로를 잡는게 아니라 imoprt하는 위치를 기준으로 경로를 정의한다

  local package 안에서 다른 local package를 import 할때 사용된다

  선언해야 하는 경로의 길이를 줄여준다는 장점이 있지만 헷갈리기 쉽고 파일위치가 변경되면 경로 위치도 변경되어야하는 단점이 있습니다. 그래서 일반적으로 absolute path를 사용하는걸 권장한다





###  Exceptions

예외 라는 뜻의 의도하지 않은 에러가 일어나는 경우를 일반적으로 exception이 일어났다고 부른다

```python
short_list = [1, 2, 3]
```

요소가 3개인 list이다 만약실수로 4번째 요소를 indexing 하게되면 IndexError가 일어난다

```python
fourth_element = short_list[3]
> 
IndexError                                Traceback (most recent call last)
<ipython-input-2-54d383a36828> in <module>()
```

해당 프로세스가 종료가 되야하지만 종료하지않고 다른 로직을 실행하게 한 후 프로그램을 계속 실행하게 하는 것을 Exception handing 이라한다. Exception handing은 `try`, `except` 구문을 사용해서 실행한다.

```python
try:
     문장1
     문장2
     ...
     문장N    
except IndexError:
     exception이 났을 경우 실행할 예외 처리코드
except Exception:
    IndexError가 아닌 다른 종류의 Exception이 발생할 경우
else:
    exception 이 나지 않을경우 실행
finally:
     Exception 여부와 상관없이 항상 마지막에 실행되는 코드
```

