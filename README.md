# 이동원 · Dongwon Lee

**Java · Spring Boot 백엔드 개발자**

Siemens Teamcenter AWC 환경에서 화면 커스터마이징과 SOA API 연동을 합니다.

[![Blog](https://img.shields.io/badge/Blog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=notion&logoColor=white)](https://www.notion.so/22d2c41c65f1808aaef7cade80995932)
[![solved.ac](https://img.shields.io/badge/solved.ac-3B82F6?style=flat-square&logo=leetcode&logoColor=white)](https://solved.ac/profile/nowgnodeel369)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)

---

## 지금 하는 일

Teamcenter Active Workspace의 선언형 프레임워크로 업무 화면을 만들고, SOA API를 붙여 데이터를 주고받습니다.
ViewModel JSON으로 화면 구조를 잡고, Service JS로 동작을 붙이는 방식입니다.

레퍼런스가 거의 없는 폐쇄적인 PLM 스택입니다. 공식 문서와 기존 코드를 읽어 동작을 역추적하는 데
시간을 많이 쓰고, 그렇게 알아낸 것들은 블로그에 정리합니다.

---

## 프로젝트

### 네스트 (Nest)

개인 · 개발 중 · [서버](https://github.com/nowgnodeel123/retirement-planner) · [웹](https://github.com/nowgnodeel123/retirement-planner-web)

**"나는 몇 살에 은퇴할 수 있는가"에 답하는 재무 앱입니다.**
자산이 지금 얼마인지 보여주는 서비스는 이미 많습니다. 네스트는 은퇴 나이를 입력받지 않고,
후보 나이를 한 살씩 올려가며 목표 생활비를 90세까지 감당할 수 있는 가장 이른 나이를 찾습니다.

**금액 단위를 명목 기준으로 통일했습니다.**
목표 생활비는 물가상승률만큼 커지는 명목 금액인데, 자산에만 실질 수익률을 적용하면
단위가 어긋나 부족분 계산이 무의미해집니다. 이 프로젝트에서 가장 오래 붙잡힌 부분입니다.

**주식과 코인은 수량도 평단도 저장하지 않습니다.**
매매 히스토리만 남기고 조회 시점에 파생 계산합니다. 거래 기록과 보유 현황이 어긋날 여지를 없앴습니다.

**외부 API가 죽어도 화면은 삽니다.**
시세와 환율을 data.go.kr, Finnhub, Upbit, 한국수출입은행에서 가져오는데,
어느 하나가 실패해도 그 부분만 조용히 비우고 나머지는 정상 렌더합니다.

`Java 21` `Spring Boot 3.4` `PostgreSQL 16` `Flyway` `Next.js` `TypeScript` `JWT`

<details>
<summary>계산 로직 — 3구간 Gap-Filling</summary>

은퇴 시점부터 90세까지를, 자산에 접근 가능해지는 시점 기준으로 세 구간으로 나눕니다.

```
은퇴 ─────────────────────────────────────────────▶ 90세
  [1. 주식/ETF만]   [2. +퇴직연금·IRP·연금저축]   [3. +국민연금]
  은퇴 ~ 55세        55세 ~ 수령개시              수령개시 ~ 90세
```

각 해에 필요한 금액에서 그 시점에 열려 있는 연금 소득을 빼고, 부족분을 주식에서 인출합니다.
이걸 은퇴 후보 나이마다 반복해 처음으로 90세까지 버티는 나이를 찾습니다.
국민연금 조기·연기수령, 퇴직연금 DB/DC, 연금저축 세액공제, 주식 양도소득세 gross-up을 반영했습니다.

</details>

### 아힘모약 (AhHimMoYak)

7인 팀 · 2024.10~12 · [서버](https://github.com/AhHimMoYak/lms_be) · [웹](https://github.com/AhHimMoYak/lms_fe) · [시연 영상](https://youtu.be/5h6VI5sSYKE)

**기업 직무교육 LMS·CMS 플랫폼입니다.**
메가존클라우드 Java 기반 SaaS 개발자 양성 과정 최종 프로젝트로, 2024 부산디지털혁신아카데미
해커톤(Dev-ton) 아이디어상을 받았습니다. 전문 개발 인력이 없는 훈련기관도 교육 과정을 직접
구성할 수 있게 만드는 것이 목표였습니다.

**코스·커리큘럼·수강신청 도메인을 맡았습니다.**
코스 목록 페이징과 상세, 강사 대시보드, 커리큘럼 CRUD, 훈련기관이 수강신청을 받고 응답하는 흐름까지.
처음에 `Contract`이던 엔티티를 `CourseProvide`로 다시 잡았습니다. "코스라는 교육 과정 자체"와
"그 코스를 특정 기관에 개설한 건"이 한 덩어리로 묶여 있어 수강신청 로직이 꼬였기 때문입니다.

**시험 기능을 Spring Boot에서 Lambda로 옮겼습니다.**
팀 목표가 기능 단위 서버리스 분리였고, 제 기능으로 그걸 실행했습니다. 퀴즈로 시작했다가
시험(Exam)으로 도메인을 다시 정의하고, 생성·수정·삭제·상세조회·목록조회·응시 제출을
기능별 람다로 쪼갰습니다. 데이터는 DynamoDB에 저장하고 `serverless.yml`도 직접 관리했습니다.

`Spring Boot` `AWS Lambda` `API Gateway` `DynamoDB` `MySQL` `Serverless Framework`

<details>
<summary>팀 아키텍처 — Spring Boot에서 서버리스로</summary>

Spring Boot 모놀리식으로 시작해, 기능 단위로 떼어내며 이벤트 기반 아키텍처로 옮겼습니다.

- **서버리스로 분리** — 사용자 관리, 게시판, 데이터 시각화, 미디어, 콘텐츠 업로드, 시험
- **ECS Fargate에 유지** — 훈련기관, 회사, 사원 서비스. 엔티티 결합이 강해 분리를 보류
- **인프라** — Serverless Framework로 IaC를 작성해 CloudFormation 스택으로 구성

인프라를 코드로 관리해 "한 번에 세팅"이 되도록 하는 것이 팀의 목표였습니다.

</details>

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
