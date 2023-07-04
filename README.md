<h2 align="middle">경북소프트웨어고등학교 출입증 관리 시스템 [ Team - SchoolPass ]</h2>

# 출입증 관리 시스템
> 기존의 방식을 개선하고 보완한 새로운 경북소프트웨어고등학교만의 출입증 관리 시스템을 구축합니다.

## 프로젝트 개요
### 개발 동기
기숙형 학교인 저희 학교는 학교 외에 기숙사에도 상벌점 제도가 있으며 이를 관리하는 것은 전부 수기, Excel 등의 방법을 사용하였으며 조금 더 편하게 관리하면 좋겠다 생각해서 진행하게 되었습니다.
### 개발 목표
데스크탑과 모바일 두 환경에서 모두 실행가능한 기존 상벌점 시스템보다 나은 환경을 목표로 합니다.

## Member
* 김진효 - (팀장), 프론트 및 총괄 | <a href="https://github.com/jinhyo-dev" target="_blank"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>
* 변예준 - 디자인, 프론트 | <a href="https://github.com/yejun178" target="_blank"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>
* 최근호 - 디자인, 백엔드 | <a href="https://github.com/cghsuw256" target="_blank"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>
* 임동주 - 백엔드(api), 프론트 | <a href="https://github.com/DocRAID" target="_blank"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>
* 김성현 - 인프라(aws), 백엔드 | <a href="https://github.com/HYUN-8265" target="_blank"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/></a>

## To be used

| 분야 | 메이커 |  | 사용목적 |
| ------------- | ---------------------- | -------------------------- | ---------------- |
| Frontend  | 장휴선 | <a href="https://ko.legacy.reactjs.org/"><img src="https://img.shields.io/badge/React-3880FF?style=flat-square&logo=Ionic&logoColor=white"/></a> | 모바일의 프론트를 담당합니다. |
| Server | 최근호 | <a href="https://docs.aws.amazon.com/"><img src="https://img.shields.io/badge/Amazon AWS-232F3E?style=flat-square&logo=Amazon AWS&logoColor=white"/></a> | 배포와 서비스를 위한 서버를 담당합니다. |
| API | 최근호 |  <a href="https://nestjs.com/"><img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=NestJS&logoColor=white"/></a>, actix [https://actix.rs]| 프로젝트에 필요한 서비스를 구현합니다. |
| DBA | 최근호  | <a href="https://www.mysql.com/"><img src="https://img.shields.io/badge/MySql-4479A1?style=flat-square&logo=MySql&logoColor=white"/></a> | 정보를 저장하기 위해 사용합니다. |
| Communication | All | <a href="https://discord.com/"><img src="https://img.shields.io/badge/Discord-5865F2?style=flat-square&logo=Discord&logoColor=white"/></a> | 보다 익숙한 환경에서의 효율적인 협업을 위해 사용합니다. |

## Skills
<a href=""><img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=white"/></a>
<a href="https://ionicframework.com/"><img src="https://img.shields.io/badge/Ionic-3880FF?style=for-the-badge&logo=Ionic&logoColor=white"/></a>
<a href="https://tauri.app/ko/"><img src="https://img.shields.io/badge/Tauri-FFC131?style=for-the-badge&logo=Tauri&logoColor=white"/></a>
<a href="https://docs.aws.amazon.com/"><img src="https://img.shields.io/badge/Amazon AWS-232F3E?style=for-the-badge&logo=Amazon AWS&logoColor=white"/></a>
<a href="https://nodejs.org/en/"><img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=Node.js&logoColor=white"/></a>
<a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=TypeScript&logoColor=white"/></a>
<a href="https://nestjs.com/"><img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=NestJS&logoColor=white"/></a>
<a href="https://www.mysql.com/"><img src="https://img.shields.io/badge/MySql-4479A1?style=for-the-badge&logo=MySql&logoColor=white"/></a>

## 프로젝트 진행
 + 프로젝트 구상과 팀원 역할 분배(2022년 7월 초 ~ 7월 말)
 + 프론트 UI/UX 구현 및 백엔드 Restful API 개발(2022년 8월 초 ~ 11월 초)
 + Ionic 프레임워크와 Tauri를 이용해 각각 웹앱과 앱으로 변환(11월 초 ~ 현재)

## 프로젝트 상세 소개

### 데이터베이스 구조
#### 유저 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| userId | INT Autoincrement | 사용자 아이디 | NN |
| grade | INT | 학년 | N |
| class | INT | 반 | N |
| number | INT | 번호 | N |
| name | VARCHAR(10) | 이름 | NN |
| phone | VARCHAR(11) | 유저 전화번호 | NN |
| account | VARCHAR(30) | 계정 아이디 | NN |
| password | CHAR(64) | 비밀번호 | NN |
| position | TINYINT | 역할을 숫자로 나누어 중,고등학생과 중,고등 교사를 구분 | NN |
| salt | VARCHAR(10) | 입력된 비밀번호와 함께 HASH함수에 넣어 주는 값 | NN |
#### 상벌점 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| pointId | INT Autoincrement | 상벌점 아이디 | NN |
| userId | INT | 사용자 아이디 | NN |
| regulateId | INT | 규정 아이디 | NN |
| reason | VARCHAR | 세부 사항 | N |
| issuer | VARCHAR | 발급자 | NN |
| created | DATE | 생성날짜 | NN |
| updated | DATE | 수정날짜 | N |
#### 규정 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| regulateId | INT | 규정 아이디 | NN |
| checked | TINYINT | 상/벌점 구분 | NN |
| regulate | VARCHAR | 규정 내용 | NN |
| score | INT | 점수 | NN |
#### 보호자 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| parentsId | INT Autoincrement | 학부모 아이디 | NN |
| userId | INT | 자녀 아이디 | NN |
| phone | VARCHAR(11) | 전화번호 | NN |
#### 파일 테이블
| Field | data type | explanation | properties |
| ---------- | -------- | --------------- | -------- |
| filename | VARCHAR(20) | 파일명 | NN |
| datatype | BOOLEAN | 데이터타입 | NN |
| created | DATE | 만들어진 시각 | NN |

## 사용자 수행 흐름도

<img src="https://cdn.discordapp.com/attachments/408947039486083072/1056855354505449572/IMG_4658.png" />

## Preview

### [Github.io 페이지](https://school-pass.github.io/schoolpass.github.io/)
