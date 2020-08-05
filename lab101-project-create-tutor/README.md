# LAB101: 프로젝트 생성 실습

## Step 1-1-00
- 구현도구 eclipse 를 실행한다. 


## Step 1-1-01 
- eclipse 에서 `eGovFrame`>`Start`>`New Web Project` 메뉴를 선택한다. 


## Step 1-1-02
- 프로젝트 생성 위저드에서 아래와 같이 입력하고 `Next` 버튼을 클릭한다.

|항목|입력내용|비고|
|:--:|:------:|:--:|
|__project name__|__lab101-project-create-tutor__|수동입력|
|__Target Runtime__|<none>|자동입력|
|__Dynamic Web Module Version__|2.5|자동입력|
|__Group Id__|__egovframe__|수동입력|
|__Artifact Id__|lab101|자동입력|
|__Version__|1.0.0|자동입력|


## Step 1-1-03
- `Generate Example` 항목을 체크하고 `Finish` 버튼을 클릭하여 프로젝트를 생성한다.


## Step 1-1-04
- 이클립스에서 생성된 `Package Explorer` 에서 프로젝트(`lab101-project-create-tutor`) 우 클릭 > `Run As` > `Maven Install` 을 클릭하여 Maven 을 실행한다.   


## Step 1-1-05
- 데이터베이스를 설정을 확인한다. (`context-datasource.xml` 설정 확인)
```xml 
<jdbc:embedded-database id="dataSource" type="HSQL">
	<jdbc:script location= "classpath:/db/sampledb.sql"/>
</jdbc:embedded-database>
```


## Step 1-1-06
- 생성한 프로젝트를 실행하여 결과를 확인한다. 
- [Eclipse 이용] `Package Explorer` 에서 프로젝트(`lab101-project-create-tutor`) 우 클릭 > `Run As` > `Run on Server` 클릭 > `Finish` 버튼 클릭 
- [오류발생시]
    - 구현도구(eclipse) 재 기동
    - `Maven Clean`, `Maven Install` 실행 후 다시 `Run On Server` 실행
