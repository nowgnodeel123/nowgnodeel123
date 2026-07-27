<div align="center">

### 이동원 · Dongwon Lee

**Java · Spring Boot 백엔드 개발자**

[![Blog](https://img.shields.io/badge/Blog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=notion&logoColor=white)](https://www.notion.so/22d2c41c65f1808aaef7cade80995932)
[![solved.ac](https://img.shields.io/badge/solved.ac-3B82F6?style=flat-square&logo=leetcode&logoColor=white)](https://solved.ac/profile/nowgnodeel369)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)

</div>

제조 기업이 설계 도면과 부품 정보를 관리하는 **PLM 시스템(Siemens Teamcenter)** 의 화면을 만들고,
서버 API를 붙이는 일을 합니다.

국내에 자료가 거의 없는 스택이라 공식 문서와 남이 짜둔 코드를 읽어 동작을 밝혀내는 게 일의 절반입니다.
알아낸 건 블로그에 정리하고, 아직 안 된 건 안 됐다고 적어둡니다.

## 경력

**2025 ~ 현재** · SI 프로젝트 백엔드 (인턴 → 정규직 전환)

- Teamcenter Active Workspace 화면 개발 — ViewModel JSON으로 구조를 잡고 Service JS로 동작을 붙이는 선언형 방식
- Teamcenter SOA API 연동

**2024** · 메가존클라우드 Java 기반 SaaS 개발자 양성 과정 수료

동서대학교 소프트웨어학과 졸업

## 프로젝트

### 네스트 (Nest)

**은퇴 가능 나이를 역산해서 알려주는 재무 앱** · 개인 · 개발 중

- 은퇴 나이를 입력받는 대신, 90세까지 버틸 수 있는 가장 이른 나이를 찾아줌
- 주식·코인은 잔고 대신 매매 히스토리만 저장하고 조회 시점에 파생 계산
- 시세·환율 API 네 곳 중 하나가 죽어도 나머지 화면은 정상 렌더
- 목표 생활비는 명목, 자산은 실질 — 단위가 어긋나면 부족분 계산이 무의미해짐

`Java 21` `Spring Boot 3.4` `PostgreSQL 16` `Flyway` `Next.js` `TypeScript`

[서버](https://github.com/nowgnodeel123/retirement-planner) · [웹](https://github.com/nowgnodeel123/retirement-planner-web)

### 아힘모약 (AhHimMoYak)

**기업 직무교육 LMS·CMS 플랫폼** · 7인 팀 · 2024.10~12 · Dev-ton 아이디어상

- 훈련기관이 과정을 열고 수강생을 받는 흐름(코스·커리큘럼·수강신청) 담당
- 시험 기능을 Spring Boot에서 Lambda 6종 + DynamoDB로 이관 — 팀 목표인 서버리스 전환을 내 기능으로 실행
- `Contract` 엔티티를 `CourseProvide`로 재정의해 "코스"와 "그 코스의 개설 건"을 분리

`Spring Boot` `AWS Lambda` `API Gateway` `DynamoDB` `MySQL` `Serverless Framework`

[서버](https://github.com/AhHimMoYak/lms_be) · [웹](https://github.com/AhHimMoYak/lms_fe) · [시연 영상](https://youtu.be/5h6VI5sSYKE)

## 기술

| | |
| :--- | :--- |
| **Backend** | <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/> <img src="https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white"/> <img src="https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white"/> |
| **Frontend** | <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/> |
| **Database** | <img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/> <img src="https://img.shields.io/badge/DynamoDB-4053D6?style=flat-square&logo=amazondynamodb&logoColor=white"/> |
| **Cloud** | <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white"/> <img src="https://img.shields.io/badge/Serverless-FD5750?style=flat-square&logo=serverless&logoColor=white"/> <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/> <img src="https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white"/> |
| **Tools** | <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/SVN-809CC9?style=flat-square&logo=subversion&logoColor=white"/> <img src="https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/> |
| **Domain** | <img src="https://img.shields.io/badge/Siemens_Teamcenter-009999?style=flat-square&logo=siemens&logoColor=white"/> |

매일 쓰는 것은 **Java · JavaScript · Oracle**입니다.
Spring Boot · PostgreSQL · Next.js는 개인 프로젝트에서, AWS 서버리스는 팀 프로젝트에서 썼습니다.
