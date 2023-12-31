<h2 align="middle">경북소프트웨어고등학교 출입증 관리 시스템 [ Team - SchoolPass ]</h2>

# 출입증 관리 시스템
> 기존의 방식을 개선하고 보완한 새로운 경북소프트웨어고등학교만의 출입증 관리 시스템을 구축합니다.

## 프로젝트 개요
### 프로젝트 주제 및 선정 배경
학교에는 정말 많은 특수실이 존재하고 이 외에도 기숙사와 같은 공간의 경우 출입 시 안전상의 이유로 학생과 선생님이 동반해야 출입을 할 수 있다는 단점이 존재하였고, 이를 해결하기 위해 프로젝트를 진행하게 되었습니다.
### 개발 및 수행 목표
학생과 교사 모두에게 편의성과 직관성을 제공하는 것이 최종적인 목표입니다.

## Member
* 최근호 - (팀장), 디자인, 백엔드 | c66182527@gmail.com | <a href="https://github.com/cghsuw256" target="_blank"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>
* 장휴선 - (팀원), 프론트 | hyuseonj771@gmail.com | <a href="https://github.com/rongtutu" target="_blank"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>


## To be used

| 분야 | 메이커 |  | 사용목적 |
| ------------- | ---------------------- | -------------------------- | ---------------- |
| Frontend  | 장휴선 | <a href="https://ko.legacy.reactjs.org/"><img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=Ionic&logoColor=white"/></a> | 모바일의 프론트를 담당합니다. |
| Server | 최근호 | <a href="https://docs.aws.amazon.com/"><img src="https://img.shields.io/badge/Amazon AWS-232F3E?style=flat-square&logo=Amazon AWS&logoColor=white"/></a> | 배포와 서비스를 위한 서버를 담당합니다. |
| API | 최근호 |  <a href="https://spring.io/projects/spring-boot"><img src="https://img.shields.io/badge/SpringBoot-6DB33F?style=flat-square&logo=SpringBoot&logoColor=white"/></a>| 프로젝트에 필요한 서비스를 구현합니다. |
| DBA | 최근호  | <a href="https://www.mysql.com/"><img src="https://img.shields.io/badge/MySql-4479A1?style=flat-square&logo=MySql&logoColor=white"/></a> | 정보를 저장하기 위해 사용합니다. |
| Communication | All | <a href="https://discord.com/"><img src="https://img.shields.io/badge/Discord-5865F2?style=flat-square&logo=Discord&logoColor=white"/></a> | 보다 익숙한 환경에서의 효율적인 협업을 위해 사용합니다. |

## Skills
<a href="https://ko.legacy.reactjs.org/"><img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=white"/></a>
<a href="https://docs.aws.amazon.com/"><img src="https://img.shields.io/badge/Amazon AWS-232F3E?style=for-the-badge&logo=Amazon AWS&logoColor=white"/></a>
<a href="https://www.mysql.com/"><img src="https://img.shields.io/badge/MySql-4479A1?style=for-the-badge&logo=MySql&logoColor=white"/></a>
<a href="https://spring.io/projects/spring-boot"><img src="https://img.shields.io/badge/SpringBoot-6DB33F?style=for-the-badge&logo=SpringBoot&logoColor=white"/></a>

## 프로젝트 진행
 + 프로젝트 구상과 팀원 역할 분배(2023년 3월 초 ~ 3월 말)
 + 프론트 UI/UX 구현 및 백엔드 Restful API 개발(2023년 4월 초 ~ 7월 초)
 + 변경된 요구사항 반영 및 안정화 작업(7월 초 ~ 현재)

## 프로젝트 상세 소개

### 데이터베이스 구조
#### 유저 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| userId | BIGNT Autoincrement | 사용자 아이디 | NN |
| grade | INT | 학년 | N |
| class | INT | 반 | N |
| number | INT | 번호 | N |
| name | VARCHAR | 이름 | NN |
| account | VARCHAR | 계정 아이디 | NN |
| password | VARCHAR | 비밀번호 | NN |
#### 출입증 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| passId | BIGINT Autoincrement | 출입증 아이디 | NN |
| userId | BIGINT | 사용자 아이디 | NN |
| placeId | BIGINT | 장소 아이디 | NN |
| teacherId | BIGINT | 교사 아이디 | NN |
| startPeriod | INT | 시작시간 | NN |
| endPeriod | INT | 종료시간 | N |
| passReason | VARCHAR | 신청사유 | N |
| passStatus | VARCHAR | 출입증상태 | NN |
| created | DATE | 생성날짜 | NN |
| updated | DATE | 수정날짜 | N |
#### 장소 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| placeId | BIGINT | 규정 아이디 | NN |
| teacherId | BIGINT | 교사 아이디 | NN |
| floor | INT | 층수 | NN |
| capacity | INT | 현재 인원 | N |
| maxCapacity | INT | 최대 인원 | NN |
| ipAddress | VARCHAR | IP주소 | NN |
| location | VARCHAR | 위치 | NN |
| locationDetail | VARCHAR | 상세위치 | N |
#### 교사 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| teacherId | BIGINT Autoincrement | 교사 아이디 | NN |
| userId | BIGINT | 사용자 아이디 | NN |
| tPermission | VARCHAR | 정/부 교사 구분 | NN |
#### 권한 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| authorityId | BIGINT | 권한 아이디 | NN |
| name | VARCHAR | 부여한 권한 이름 | NN |
| member | BIGINT | 사용자 | NN |

## 사용자 수행 흐름도

<img width="3312" alt="schoolpass" src="https://github.com/school-pass/.github/assets/83445334/66015d28-f8b0-462f-9268-43c329b24333">

## 프로젝트 추진 결과
### 수행 과정 및 결과 분석
> 초기 계획과 달리 상당 부분 변경점이 있었고, 이로 인해 DB 구조가 바뀌고 UI/UX도 바꾸는 등의 여러 에로 사항이 생겼지만 백엔드의 경우 기본적인 기능 구현이 모두 성공적으로 끝났고 프론트의 경우는 기술 스택이 개발 도중 여러번 바뀌며 완성시키지 못하였다.

### 유지 보수 계획
AWS를 프로젝트에 사용한 만큼 유지 보수 중 유지는 해결되었다 생각된다. 또한, 보수의 부분도 Github의 코드를 업로드 후 clone 하는 방식으로 지속적인 에러 수정 및 관찰을 할 생각이다.

## 레이아웃 등 더 알아보기
### [Github.io 페이지](https://school-pass.github.io/schoolpass.github.io/)
