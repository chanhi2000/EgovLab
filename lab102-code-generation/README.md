# LAB102: Code Generation 실습

## Step 1-2-01. 

 - `lab102-code-generation` 프로젝트를 오픈한다.

## Step 1-2-02. 

 - `Package Explorer`에서 생성된 `lab102-code-generation` 의 데이터베이스를 실행.

 ![img1-2-02][img1-2-02]

 - `DATABASE` > `db` 마우스 우클릭 
 - `path tools` > `Command Line Shell` 선택
 - 커맨드 창에서 `runHsqlDB.cmd` 실행


## Step 1-2-03.

 - `Data Source Explorer`에서 HSQLDB에 Connect 한다.

![img1-2-03][img1-2-03]

## Step 1-2-04. 

 - 이클립스 `Window` > `Show View` > `Other…` 를 선택
 - `Show View` 창을 연다. 
 - 프로젝트를 선택한 상태에서, 대화창에서 `eGoveFramework` >
`eGovFrame Templates` 를 더블클릭한다

![img1-2-04][img1-2-04]


## Step 1-2-05.

 - `lab102-code-generation` 프로젝트를 선택
 - `eGovFrame Templates` 뷰에서 `eGovFrame Templates` > `CRUD` > `CRUD Program` 을 더블클릭 

![img1-2-05][img1-2-05]


## Step 1-2-06.

 - `PUBLIC` > `SAMPLE` 테이블을 선택한 후 `NEXT`를 클릭.

![img1-2-06][img1-2-06]


## Step 1-2-07.
 -  소스코드 자동생성 디렉토리 정보를 입력하고 `Finish` 버튼을 클릭.

|항목|입력내용|비고|
|:--:|:------:|:--:|
|__Resource(SQLMap) Folder__|`/lab102-code-generation/src/main/resources/egovframework/sqlmap/example`|.|
|__DAO Package__|`egovframework.example.sample.service.impl`|.|
|__VO Package__|`egovframework.example.sample.service`|.|
|__Service Package__|`egovframework.example.sample.service`|.|
|__Service Impl Package__|`egovframework.example.sample.service.impl`|.|
|__Controller Package__|`egovframework.example.sample.web`|.|
|__JSP Folder__|`/lab102-code-generation/src/main/webapp/WEB-INF/jsp/egovframework/example`|.|

![img1-2-07][img1-2-07]

## Step 1-2-08.
 
 - `src/main/resources` 에서 `egovframework.sqlmap.example` 패키지의 `sql-map-config.xml` 파일을 열고 
 - 생성된 `Sample_SQL.xml` 파일을 추가되어 있는지 확인.

## Step 1-2-09. 
 
 - 생성한 프로젝트를 실행.

### Eclipse 이용
 
 - `Package Explorer` 에서 프로젝트 (`lab102-code-generation`) 우클랙 
 - `Run As` > `Run on Server` 클릭 > `Finish` 버튼 클릭

### 오류발생시

 - 구현도구(eclipse) 재 기동
 - `Maven Clean`, `Maven Install` 실행 후 다시 `Run On Server` 실행
 

## 1-2-10.
 - 웹브라우저를 통하여 생성한 소스의 기능을 확인한다.

### 접속 URL
 - [http://localhost:8080/lab102-code-generation/sample/SampleList.do][url]

[img1-2-03]: ../imgs/lab102-2-03.png
[img1-2-04]: ../imgs/lab102-2-04.png
[img1-2-05]: ../imgs/lab102-2-05.png
[img1-2-06]: ../imgs/lab102-2-06.png
[img1-2-07]: ../imgs/lab102-2-07.png

[url]: http://localhost:8080/lab102-code-generation/sample/SampleList.do