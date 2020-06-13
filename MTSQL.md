# MTSQL

[MYSQL  강좌 링크]( https://opentutorials.org/course/3161)

### MYSQL 의 파일 위치

 `C:\Bitnami\wampstack-7.4.6-1\mysql\bin` 이후  `mysql -uroot -p` 입력



### 용어 

표 = table

x축 = row, record

y축 = column



### 스키마관련 명령어

`CREATE DATABASE (스키마이름);`  = 생성

`DROP DATABASE (스키마이름);` = 삭제

`SHOW DATABASES;` = 저장되어있는 스키마 목록을본다

`USE (스키마이름);` = 스키마 사용

`DESC (테이블이름);` = 테이블의 구성을 보여줌



### 테이블 만들기

> `REATE TABLE opentutorials.topic (`
> `'id' INT(11) NOT NULL AUTO_INCREMENT,`
> `'title' VARCHAR(100) NOT NULL,`
> `'description' TEXT NULL,`
> `'created' DATETIME NOT NULL,`
> `'author' VARCHAR(30) NULL,`
> `'profile' VARCHAR(100) NULL,`
> `PRIMARY KEY (id)`
> `);`

총 column은 6개 

`INT(11)` = 정수형(11은 한번에 목록을보는 제한횟수) , `NOT NULL` = 생략불가능 , `AUTO_INCREAMENT` = 자동적으로 값이 1씩추가

`VARCHAR(100)` = 글자형변수(100자리까지입력가능) , `TEXT` = 텍스트를 입력한다(본문), `NULL` = 생략가능

`DATETIME` = 년월일시분초 입력가능,  ``PRIMARY KEY(id)` = id값을 프라이머리키로 지정



### INSERT 

##### 테이블에 내용추가

`INSERT INTO topic (title,description,created,author,profile) VALUES('MYSQL','MYSQL is ...',NOW(),'egoing','developer' );`

`INSERT INTO topic`  = topic이란 스키마에 값을 추가한다.

`topic(title,description,created,author,profile)`

`VALUES('MYSQL','MYSQL is ...',NOW(),'egoing','developer' )`

밸류에 순서대로 값을 입력, `NOW()` = 현재시간



### SELECT

##### 테이블 내용읽기

`SELECT * FROM (테이블이름);`  = 테이블의 내용을 읽는다

`*`은 테이블안의 모든 내용을 뜻함

`SELECT id,title FROM topic WHERE author='egoing';`

= topic 의  author가 egoing인 값의 id,title 값을 읽는다. 

`SELECT * FROM topic WHERE author='egoing' ORDER BY id DESC LIMIT 2;`

= topic의 author가 egoing 인 모든값중 2개만 읽는다



### UPDATE

##### 테이블 내용 수정

`UPDATE topic SET title='hanna', description='hahanna', author='hanna' WHERE id=2;`

= topic의 id가 2인 자료의 title을 hanna, description을 hahanna, author을 hanna 로 바꾼다



### DELETE

##### 테이블 내용삭제 

`DELETE FROM topic WHERE id=5;`

=id 가 5인 값을 삭제 

딜리트는 신중하게사용할것 한번사용으로 인생이 바뀌게될수있다.



### 테이블 분리하기

##### 관계형 데이터베이스의 필요성

`SELECT * FROM topic LEFT JOIN author ON topic.author_id  = author.id;`

= topic 과 author의 테이블을 보여준다 topic의 author_id 값과 author 의 id 값은 같다 (같이목록으로 보여줌)



### SQL JOIN

##### JOIN 명령어의 종류를 알아보자

[JOIN밴다이어그램](www.sql-joins.leopard.in.ua)

- **LEFT JOIN** (중요)

  `SELECT * FROM tableA LEFT JOIN tableB ON A.key = B.key;`

  `SELECT * FROM tableA LEFT JOIN tableB ON A.key = B.key LEFT JOIN tableC ON  tableB.key = tableC.key;`

  `SELECT key1,key2,key3 AS 별명 FROM tableA LEFT JOIN tableB ON A.key = B.key LEFT JOIN tableC ON  tableB.key = tableC.key;`

  `SELECT key1,key2,key3 AS 별명 FROM tableA LEFT JOIN tableB ON A.key = B.key LEFT JOIN tableC ON  tableB.key = tableC.key WHERE tableA.key =1;`

  

- **INNER JOIN**

  양쪽다 존재하는 결과물만 출력 (NULL 값을 가져오지 않음)

  `SELECT * FROM tableA INNER JOIN tableB ON A.key = B.key;`

  `SELECT * FROM tableA INNER JOIN tableB ON A.key = B.key INNER JOIN tableC ON  tableB.key = tableC.key;`

- **FULL OUTER JOIN**

  오른쪽에만 있는 값, 왼쪽에만 있는값 이 테이블 기준으로 밑에 결과값이 추가로 출력됨

  `(SELECT * FROM tableA LEFT JOIN tableB ON A.key = B.key;) UNION (SELECT * FROM tableA LIGHT JOIN tableB ON A.key = B.key;)`

- **EXCLUSIVE JOIN**

  tableA 에만 있는 값을 출력

  `SELECT * FROM tableA LEFT JOIN tableB ON tableA.key = tableB.key WHERE  tableB.key is NULL`

  

##### 테이블 분해,병합 를 좀더 알고싶으면 database modeling,database normalization(정규화) 를 검색할것

