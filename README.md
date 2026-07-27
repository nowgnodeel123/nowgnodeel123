<div align="center">

### 👨‍💻 이동원 · Dongwon Lee

**Java · Spring Boot 백엔드 개발자**

<br/>

[![Blog](https://img.shields.io/badge/Blog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=notion&logoColor=white)](https://www.notion.so/22d2c41c65f1808aaef7cade80995932)
[![solved.ac](https://img.shields.io/badge/solved.ac-3B82F6?style=flat-square&logo=leetcode&logoColor=white)](https://solved.ac/profile/nowgnodeel369)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)

</div>

## 소개

Java와 Spring Boot로 API를 만드는 백엔드 개발자입니다. 실무 1년차입니다.

현재 **Siemens Teamcenter Active Workspace** 화면 개발과 SOA API 연동을 담당하고 있습니다.
Teamcenter는 제조 기업이 설계 도면과 부품 정보를 관리하는 PLM 시스템입니다.
공개된 자료가 적어, 공식 문서와 기존 코드를 읽어 동작을 파악하는 방식으로 일합니다.

## 프로젝트

### 네스트 (Nest)

은퇴 가능 나이를 역산해서 알려주는 재무 앱 · 개인 · 개발 중

- 은퇴 나이를 입력받지 않고, 후보 나이를 한 살씩 올려 90세까지 버티는 가장 이른 나이를 계산
- 주식·코인은 잔고를 저장하지 않고 매매 히스토리에서 조회 시점에 파생 계산
- 시세·환율을 외부 API 네 곳에서 수집, 일부 실패해도 나머지 화면은 정상 렌더
- Flyway로 스키마 버전 관리, `ddl-auto: validate`로 고정
- 명목·실질 혼용 문제 해결: 목표 생활비는 명목, 자산 수익률은 실질이라 단위가 어긋나
  부족분 계산이 무효화됨 → 전 계산을 명목 기준으로 통일

`Java 21` `Spring Boot 3.4` `PostgreSQL 16` `Flyway` `Next.js` `TypeScript` `Railway` `Vercel`

[서버](https://github.com/nowgnodeel123/retirement-planner) · [웹](https://github.com/nowgnodeel123/retirement-planner-web)

### 아힘모약 (AhHimMoYak)

기업 직무교육 LMS·CMS 플랫폼 · 7인 팀 · 2024.10~12 · Dev-ton 아이디어상

- 코스·커리큘럼·수강신청 도메인 담당 — 훈련기관이 과정을 열고 수강생을 받는 흐름
- 시험 기능을 Spring Boot에서 Lambda 6종 + DynamoDB로 이관, `serverless.yml` 작성 및 배포
- `Contract` 엔티티에 "교육 과정"과 "그 과정의 개설 건"이 섞여 수강신청 로직이 꼬여
  `CourseProvide`로 분리

`Spring Boot` `AWS Lambda` `API Gateway` `DynamoDB` `MySQL` `Serverless Framework`

[서버](https://github.com/AhHimMoYak/lms_be) · [웹](https://github.com/AhHimMoYak/lms_fe) · [시연 영상](https://youtu.be/5h6VI5sSYKE)

## 경력

**2025 ~ 현재** · SI 프로젝트 백엔드 (인턴 → 정규직 전환)
Teamcenter Active Workspace 화면 개발, SOA API 연동

**2024** · 메가존클라우드 Java 기반 SaaS 개발자 양성 과정 수료

**동서대학교** 소프트웨어학과 졸업

## 기술

| | |
| :--- | :--- |
| **Backend** | <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/> <img src="https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white"/> <img src="https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white"/> |
| **Frontend** | <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/> |
| **Database** | <img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/> <img src="https://img.shields.io/badge/DynamoDB-4053D6?style=flat-square&logo=amazondynamodb&logoColor=white"/> |
| **Cloud** | <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white"/> <img src="https://img.shields.io/badge/Serverless-FD5750?style=flat-square&logo=serverless&logoColor=white"/> <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/> <img src="https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white"/> |
| **Tools** | <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/SVN-809CC9?style=flat-square&logo=subversion&logoColor=white"/> <img src="https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/> |
| **Domain** | <img src="https://img.shields.io/badge/Siemens_Teamcenter-009999?style=flat-square&logo=siemens&logoColor=white"/> |

