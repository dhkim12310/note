# Git, Source tree

[강좌 링크]( https://opentutorials.org/course/1492)

### 파일 올리기 /취소

- working copy = 저장소에 넣기전 파일 공간

- staging area = 저장소에 올라가기직전 공간
- repository = 저장소

파일올리기 = working copy -> add -> staging area -> commit -> repository

수정사항취소 = 마우스오른쪽 -> Discard

### reset

reset current branch to this commit(Hard) = 저장파일 완전 삭제

reset current branch to this commit(Mixed) = 삭제되지만 working copy로 이동

### revert

버전을 삭제하지 않으면서 수정되기전 상태로 되돌아감

reverse commit 을 클릭

### branch

##### 실험적, 불확실한 코드를 짤때 엎어질것을 각오하고 다른버전의 코드를 짤때 사용

- branch 버튼을 클릭하면 만들수 있다.

- 브랜치 병합

  오른쪽클릭 merge master into current branch 클릭

- 브랜치 간의 출동 해결

  <<<<<<<< master

  =========

  \>>>>>>>>> 브랜치2

  이런식으로 코드가 출동할때 해결후

  Recole Conflicts -> Mark Resolved 클릭  ->Commit

- 브랜치 출동의 예방

  자주 브랜치를 동기화 해서 작은 출동이 일어날때 해결해주는것이 좋다.

  Resolve Using 'Mine' = 현재 브랜치에있었던 내용을 채택
  Resolve Using 'Theirs' = 마스터(다른)브랜치 내용을 채택



### 원격 저장소

- 원격 저장소 종류

  Github, Gitlab, Yobi 등이있다

- 원격 저장소 만들기

  메뉴상단 Repository -> Add remote 클릭
   왼쪽 메뉴에 REMOTES -> origin 메뉴가 생김
   push 버튼으로 깃허브에 저장

- push 

  연결된 원격저장소로 자료가 저장

- pull

  연결된 원격저장소에서 자료를 받아옴 

- 원격 저장소 복제

  상단 메뉴바 + -> Clone,  add , create 가 있음 -> github (clone or cownload )URL 복사 -> 로컬경로 지정

- diff = 브랜치를할때 서로다른 코드의 차이점을 발견해주는 소프트웨어
  http://en.wikipedia.org/wiki/Comparison_of_file_comparison_tools

  - beyond compare 강력한 기능을 가지고 있지만 유료다. 
     http://www.scootersoftware.com/

  다운후 toll -> 옵션 -> diff
  브랜치의 공통된 조상 = base
  자신이 현재 선택한 브랜치 = local
  그외 브랜치 = remote

- stash

  아직 끝나지않은 작업을 안전한곳에 보관
   상단바에 stash 버튼 -> 메모 ->  왼쪽 메뉴바에 뜸
   오른쪽클릭 apply stash 'On master: ~' 스태쉬를 적용

- Tag

  책갈피기능 

  브랜치만들때 speccified commit 란에 태그이름을 입력

  확인하려면 github의 Releases 클릭

- ignore

  버전관리에서 제외할 파일 만들기

  .bak 파일같은걸 오른쪽 클릭  
   Ignore exact filename(s) 이파일과 같은 이름을 무시
   Ignore all files with this extension 확장자 같은 파일 무시
   Ignore everything beneath 
   Ignore custom patterm 좀더 세부적으로 이그노

  .gitignere 파일 생김 (이그노 시킬파일 조건을 저장)
   commit 하면됨
   이그노를 세부적으로 하려면 glob 구글검색
   gitognore.io 이그노 에디터(이그노 할 코드를 쉽게 작성 해줌)

- 환경파일의 관리
   php 로 id password 틀만 만들고 templite 파일 만듬 
   그걸 이그노 한다음 개인 아이디 작성