# 이동원 · Dongwon Lee

**Java · Spring Boot 백엔드 개발자**
Siemens Teamcenter AWC 환경에서 화면 커스터마이징과 SOA API 연동을 합니다.

[![Blog](https://img.shields.io/badge/Blog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=notion&logoColor=white)](https://www.notion.so/22d2c41c65f1808aaef7cade80995932)
[![solved.ac](https://img.shields.io/badge/solved.ac-3B82F6?style=flat-square&logo=leetcode&logoColor=white)](https://solved.ac/profile/nowgnodeel369)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)

---

## 지금 하는 일

Teamcenter Active Workspace 화면 개발과 SOA API 연동.
ViewModel JSON으로 구조를 잡고 Service JS로 동작을 붙입니다.

레퍼런스가 거의 없는 스택이라, 문서와 기존 코드로 동작을 역추적하고 블로그에 정리합니다.

---

## 프로젝트

### 네스트 (Nest)

은퇴 가능 나이를 역산해서 알려주는 재무 앱 · 개인 · 개발 중

- 은퇴 나이를 입력받지 않고, 90세까지 버티는 가장 이른 나이를 역산
- 주식·코인은 잔고 대신 매매 히스토리만 저장하고 조회 시점에 파생 계산
- 시세·환율 API 4곳 중 하나가 죽어도 나머지 화면은 정상 렌더
- 명목 금액과 실질 수익률의 단위를 맞추는 데 가장 오래 걸림

`Java 21` `Spring Boot 3.4` `PostgreSQL 16` `Flyway` `Next.js` `TypeScript`

[서버](https://github.com/nowgnodeel123/retirement-planner) · [웹](https://github.com/nowgnodeel123/retirement-planner-web)

### 아힘모약 (AhHimMoYak)

기업 직무교육 LMS·CMS 플랫폼 · 7인 팀 · 2024.10~12 · **Dev-ton 아이디어상**

- 코스·커리큘럼·수강신청 도메인 담당 (Spring Boot)
- 시험 기능을 Spring Boot에서 Lambda 6종으로 분리, DynamoDB 전환
- `Contract` 엔티티를 `CourseProvide`로 재정의해 코스와 개설 건을 분리
- 팀 목표였던 기능 단위 서버리스 전환을 내 기능으로 실행

`Spring Boot` `AWS Lambda` `API Gateway` `DynamoDB` `MySQL` `Serverless Framework`

[서버](https://github.com/AhHimMoYak/lms_be) · [웹](https://github.com/AhHimMoYak/lms_fe) · [시연 영상](https://youtu.be/5h6VI5sSYKE)

---

## 기술

| | |
| :--- | :--- |
| **Backend** | <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/> <img src="https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white"/> <img src="https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white"/> |
| **Frontend** | <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/> |
| **Database** | <img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/> <img src="https://img.shields.io/badge/DynamoDB-4053D6?style=flat-square&logo=amazondynamodb&logoColor=white"/> |
| **Cloud** | <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white"/> <img src="https://img.shields.io/badge/Serverless-FD5750?style=flat-square&logo=serverless&logoColor=white"/> <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/> <img src="https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white"/> |
| **Tools** | <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/SVN-809CC9?style=flat-square&logo=subversion&logoColor=white"/> <img src="https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/> |

실무에서 매일 쓰는 것은 **Java · JavaScript · Oracle**입니다.
Spring Boot · PostgreSQL · Next.js는 개인 프로젝트에서, AWS 서버리스는 팀 프로젝트에서 썼습니다.
