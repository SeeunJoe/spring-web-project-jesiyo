<h1 align="center">
  WEB프로젝트 (제시요)
</h1>


<div align="center">
  <img src="https://github.com/user-attachments/assets/19080314-fcf1-4447-91b2-b7d443ecb456" width="800">
</div>

## 개요 : 중고 거래 경매 사이트
<br>

<p align="center">
  불특정 다수의 입찰자들이 가격 경쟁을 통해 중고 물품을 쟁취할 수 있는 웹사이트 <br>
  실시간 경매를 통해 구입 및 판매 가능 <br>
  경매를 통한 구매 욕구 자극, 사용자의 높은 스릴감과 만족도 제공
</p>

<br>

---

## 프로젝트 특징
<br>
- 상세 검색 및 필터링, 각종 편의 서비스 :<br><br>
  다양한 검색 옵션과 필터를 제공하여 사용자가 원하는 상품을 쉽게 찾을 수 있게 합니다.<br><br>
- 더 안전한 거래 환경을 제공 :<br><br>
  최종 낙찰이 된 물품에 대해 판매자와 구매자가 모두 구매 확정 버튼을 눌러야 정상적으로 거래가 종료됩니다.<br><br>

## 시연 영상


<br><br>
[![Watch the video](https://img.youtube.com/vi/jFeC4igBcF8/0.jpg)](https://www.youtube.com/watch?v=jFeC4igBcF8)

<br><br>



## 팀원
- 박무현(팀장) [![박무현](https://img.shields.io/badge/GitHub-박무현-orange)](https://github.com/MooHyunPark)
- 송승현 [![송승현](https://img.shields.io/badge/GitHub-송승현-blue)](https://github.com/seunghyeon22)
- 조세은 [![조세은](https://img.shields.io/badge/GitHub-조세은-red)](https://github.com/SeeunJoe)
- 김인범 [![김인범](https://img.shields.io/badge/GitHub-김인범-green)](https://github.com/kiminbeam)
- 이나겸 [![이나겸](https://img.shields.io/badge/GitHub-이나겸-yellow)](https://github.com/NakyeomLee)
<br>





## 통합 구현 기능



### 유저 관련 기능
- 로그인, 회원가입, 아이디 비밀번호 찾기, 내 정보 수정, 입금과 출금(약식)
### 경매 관련 기능
- 입찰, 재입찰, 취소, 물품 등록
### 신고 기능
- 판매자 / 구매자 신고
### 관리자 
- 카테고리 관리, 거래 관련 내역 확인, 신고 내용 처리
<br>

<br>


## 내가 구현한 내용
- 로그인 페이지 페이지
- 회원가입 페이지 페이지
- 아이디, 비밀번호 찾기 페이지
- 내 정보 수정 페이지
- 입출금 페이지
  
  
<br>
<br>

## 보완할 점

<br>
시간 부족으로 skip 한 내용 : 
<br><br>

- 장시간 판매자 및 구매자가 아무런 행동을 취하지 않을 때 > 강제 경매 취소 기능을 통해 경매 취소 해야하나 미구현
- 입금 출금을 약식으로 진행

<br>
<br>
컨벤션을 만들었으나 제대로 공유되지 않은 내용 :
<br><br>

- Http 1.0 방식으로 작성하기로 했으나(get, post만 사용) put, delete 등의 다른 http 메서드를 사용한 부분
- 인증이 필요한 경로에 /s를 붙이지 않은 내용. (추후 일일이 제가 다시 변경하게되어 불필요하게 시간이 낭비됨)
<br><br><br>

## 트러블슈팅
<br><br>

※ 미리 만든 커스텀 예외 클래스들은 html을 반환

1. json 응답을 원하는 자바 스크립트 비동기 요청이 다수 존재하였습니다.
2. 위 요청에서 문제가 생겼을 때 json으로 응답하는 것이 아닌, 만들어놓은 커스텀 예외를 throw 하는 경우가 다수 있었습니다. (html이 반환됨)
3. 1번의 경우 json 응답 또는 평문을 날려야만 정상적으로 작동하기 때문에 예외 발생 시 화면에 아무것도 나오지 않았습니다.
4. 해당 내용의 원인을 모두 찾아 분석하고 수정 후 팀원들에게 해당 내용을 공유하였습니다.

<br><br>

<div align="center">
  <img src="https://github.com/user-attachments/assets/40942f82-b80b-414e-9d26-088731c357ec" width="250">

</div>

<br><br><br>
위의 문제가 발생한 이유 : 예외 관련된 테스트가 제대로 진행되지 않았습니다.

<br>

프로젝트 종료 이후 생각 : Validation을 활용해 데이터가 처리되는 방식을 익히고 토큰 기반 인증을 도입하며 보안을 강화했습니다. API를 연동하며 API 설계 원리와 데이터 처리 흐름을 보다 명확히 이해하게 되었습니다. API를 사용하니 기대 이상의 좋은 결과가 나와 만족도가 높았습니다. 단위 테스트는 어렵게 느껴져 단위 테스트를 꾸준히 습관화하여 개발 완성도를 높이고 싶습니다.

<br><br>


## 느낀점
<br><br>

- 컨벤션: <br>
로직을 구현 시 Controller, Service, Repository 등 계층의 역할을 구분하고 데이터 반환 시 DTO를 사용하는 등의 컨벤션을 사전에 정한 덕분에 팀원 간 소통이 훨씬 원활해졌습니다.<br>
코드 수정이 필요할 때에도 일관된 구조 덕분에 효율적으로 작업할 수 있었습니다.
<br><br>

- 소통 : <br>
프로젝트를 진행하면서 팀원들과 자주 소통하는 것이 완성도에 많은 영향을 준다는 것을 느꼈습니다. 서로 놓친 부분은 대화를 통하여 다시 확인하며 오류 발생 시 소통으로 빠르게 해결할 수 있었습니다.<br>




## 기타

---

## 프로젝트 업무 관리
<br>

- 업무 진행 과정은 업무 보드를 통해 관리하고 확인

<div align="center">
  <img src="https://github.com/user-attachments/assets/fcc350f9-dd29-4561-8896-636f8a71fec4" width="800">
</div>

<br><br><br>

- 진행 중 어려웠던 부분은 한곳에 모아서 서로 공유할 수 있도록 관리
  
<div align="center">
  <img src="https://github.com/user-attachments/assets/f842822b-27c8-4d01-8edc-c0da6d2e37b9" width="800">
</div>
<br><br>


## 프로젝트 기간
<br>

- 2024년 12월 2일 ~ 2024년 12월 18일 (16일간)

<br>
<br>

## ERD
<div align="center">
  <img src="https://github.com/user-attachments/assets/656f46cb-c897-4376-9022-ac4ab7292d2f" width="800">
</div>
<br>
<br><br><br><br>


## 기술 스택
### Backend
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
<img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
![Gradle](https://img.shields.io/badge/Gradle-02303A.svg?style=for-the-badge&logo=Gradle&logoColor=white)

### Frontend
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white)

### IDE
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJIDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white)

### 협업도구
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)

### 데이터베이스
<img src="https://img.shields.io/badge/H2DB-31A8FF?style=for-the-badge&logo=H2DB&logoColor=white">
<br><br>





### Dependencies
```
implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
implementation 'org.springframework.boot:spring-boot-starter-mustache'
implementation 'org.springframework.boot:spring-boot-starter-security'
implementation 'org.springframework.boot:spring-boot-starter-validation'
implementation 'org.springframework.boot:spring-boot-starter-web'
compileOnly 'org.projectlombok:lombok'
developmentOnly 'org.springframework.boot:spring-boot-devtools'
runtimeOnly 'com.h2database:h2'
annotationProcessor 'org.projectlombok:lombok'
testImplementation 'org.springframework.boot:spring-boot-starter-test'
testImplementation 'org.springframework.security:spring-security-test'
testRuntimeOnly 'org.junit.platform:junit-platform-launcher'
implementation group: 'com.google.code.gson', name: 'gson', version: '2.11.0'
implementation 'net.minidev:json-smart:2.4.1'
```
<br><br>






