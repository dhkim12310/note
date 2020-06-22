# HTML,CSS

### Position

레이아웃을 배치하거나 객체를 원하는 위치에 놓을수 있는 기능

- **static** (기본값) : 위치를 지정하지 않을 때 사용한다.

- **relative**: 위치를 계산할때 static의 원래 위치부터 계산한다. CSS를 활용해 top,bottom,left,right 로 위치를 조정할수 있다.

- **absolute**: 원래 위치와 상관없이 위치를 지정할 수 있다. 단, 가장 가까운 상위 요소를 기준으로 위치가 결정 된다.

  ​                    CSS를 활용해 top,bottom,left,right 로 위치를 조정할수 있다.

- **fixed**: 원래 위치와 상관없이 위치를 지정할 수 있다. 하지만 상위 요소에 영향을 받지 않기 때문에 화면이 바뀌더라도 고정된 위치를

  ​			설정 할 수 있다.   브라우저 화면의 상대 위치를 기준으로 위치가 결정된다. CSS를 활용해 top,bottom,left,right 로 위치를

  ​            조정할수 있다.





### Display

(inline, inline-block, block)

display 속성은 그 값에 따라서 웹페이지를 보고 있는 사용자에게 특정 요소를 어떻게 보여줄지 결정된다.

- **block**: 이 요소 바로 옆(좌우측)에 다른 요소를 붙여넣을 수 없다 대표적인 태그로는 p 태그와 form 태그 header 태그 footer 태그 section 태그등이 있다.
- **inline:** 요소는 요소끼리 서로 한 줄에, 바로 옆에 위치할 수 있다 대표적으로 span 태그와 a 태그가 있다.
- **inline-block:** display 속성이 inline-block으로 지정된 엘리먼트는 기본적으로 inline 엘리먼트처럼 전후 줄바꿈 없이 한 줄에 다른 엘리먼트들과 나란히 배치된다. 하지만 inline 엘리먼트에서 불가능하던 width와 height 속성 지정 및 margin과 padding 속성의 상하 간격 지정이 가능하다.



### Float 

주로 이미지 주변에 텍스트를 감싸기 위해 만들어진 프로퍼티이다. 정렬을 위해 만들어졌다. 각 객체를 오른쪽과 왼쪽에 정렬하여 문서에 배치할때 쓰인다.

- **none**: 띄우지 않음

- **left**: 왼쪽부터 시작한 후 입력값의 자리를 할당 받는다. 

- **right**: 오른쪽부터 시작한 후 입력값의 자리를 할당 받는다.

- **initial**: 기본값으로 설정함

- **inherit**: 부모 요소로 부터 상속함

  

### **Clear**

float 속성 때문에 객체가 다음줄로 넘어가지 않을때 사용한다. clear 속성이 지정된 영역 이후로는 더 이상 float가 작동하지 않는다.

- **none**: 기본 값
- **float** : left 속성을 해제한다.
- **right**: right 속성을 해제한다.
- **both**: left, right 속성을 둘 다 해제한다.