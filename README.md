<div align="center">

### 이동원 · Dongwon Lee

**Java · Spring Boot 백엔드 개발자**

[![Blog](https://img.shields.io/badge/Blog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=notion&logoColor=white)](https://www.notion.so/22d2c41c65f1808aaef7cade80995932)
[![solved.ac](https://img.shields.io/badge/solved.ac-3B82F6?style=flat-square&logo=leetcode&logoColor=white)](https://solved.ac/profile/nowgnodeel369)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)

</div>

## 검색해도 답이 안 나오는 스택에서 일합니다

**Siemens Teamcenter**는 제조 기업이 설계 도면과 부품 정보를 관리하는 PLM 시스템입니다.
국내 사용자가 적어 블로그 글도, 스택오버플로 답변도 거의 없습니다.
그래서 공식 문서와 선임이 짜둔 코드를 읽어 동작을 역추적하는 것이 일의 절반입니다.

대신 도메인이 좁습니다. 그 폭은 개인 프로젝트로 직접 만들고 있습니다.

## 프로젝트

### 네스트 (Nest)

**은퇴 가능 나이를 역산해서 알려주는 재무 앱** · 개인 · 개발 중

기존 자산관리 앱이 "지금 내 자산이 얼마인가"를 보여준다면,
네스트는 "나는 몇 살에 은퇴할 수 있는가"에 답합니다.
은퇴 나이를 입력받지 않고, 후보 나이를 한 살씩 올려가며 90세까지 버티는 가장 이른 나이를 찾습니다.

- 주식·코인은 잔고 대신 매매 히스토리만 저장하고, 조회 시점에 파생 계산
- 시세·환율 API 네 곳 중 하나가 죽어도 나머지 화면은 정상 렌더
- Flyway로 스키마를 버전 관리하고 `ddl-auto: validate`로 고정

**가장 오래 붙잡은 것** — 목표 생활비는 물가만큼 커지는 명목 금액인데, 자산에만 실질 수익률을
적용하면 단위가 어긋나 부족분 계산 자체가 무의미해집니다. 전 계산을 명목 기준으로 통일했습니다.

`Java 21` `Spring Boot 3.4` `PostgreSQL 16` `Flyway` `Next.js` `TypeScript`

[서버](https://github.com/nowgnodeel123/retirement-planner) · [웹](https://github.com/nowgnodeel123/retirement-planner-web)

### 아힘모약 (AhHimMoYak)

**기업 직무교육 LMS·CMS 플랫폼** · 7인 팀 · 2024.10~12 · Dev-ton 아이디어상

전문 개발 인력이 없는 훈련기관도 교육 과정을 직접 구성할 수 있게 만드는 것이 목표였습니다.
저는 훈련기관이 과정을 열고 수강생을 받는 흐름 — 코스·커리큘럼·수강신청을 맡았습니다.

- 시험 기능을 Spring Boot에서 Lambda 6종 + DynamoDB로 이관
- 팀 전체 목표였던 기능 단위 서버리스 전환을, 내 기능으로 직접 실행
- `serverless.yml`을 직접 관리하며 배포까지 담당

**가장 잘한 판단** — `Contract`이라는 한 엔티티에 "코스라는 교육 과정"과 "그 코스를 특정 기관에
개설한 건"이 섞여 있어 수강신청 로직이 꼬였습니다. `CourseProvide`로 분리해 정리했습니다.

`Spring Boot` `AWS Lambda` `API Gateway` `DynamoDB` `MySQL` `Serverless Framework`

[서버](https://github.com/AhHimMoYak/lms_be) · [웹](https://github.com/AhHimMoYak/lms_fe) · [시연 영상](https://youtu.be/5h6VI5sSYKE)

## 경력

**2025 ~ 현재** · SI 프로젝트 백엔드 (인턴 → 정규직 전환)
Teamcenter Active Workspace 화면 개발과 SOA API 연동

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

매일 쓰는 것은 **Java · JavaScript · Oracle**입니다.
Spring Boot · PostgreSQL · Next.js는 개인 프로젝트에서, AWS 서버리스는 팀 프로젝트에서 썼습니다.

각 레포 README에 무엇이 되고 무엇이 아직 안 됐는지 적어두었습니다.
