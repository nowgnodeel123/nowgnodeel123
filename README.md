# 이동원 &nbsp;·&nbsp; Dongwon Lee

**Java · Spring Boot 백엔드 개발자입니다. 실무 1년차.**

현재 Siemens Teamcenter Active Workspace(AWC) 환경에서
화면 커스터마이징과 SOA API 연동을 담당하고 있습니다.

[블로그](https://velog.io/@nowgnodeel123/posts) &nbsp;·&nbsp;
[포트폴리오](https://www.notion.so/22d2c41c65f1808aaef7cade80995932) &nbsp;·&nbsp;
[solved.ac](https://solved.ac/profile/nowgnodeel369) &nbsp;·&nbsp;
nowgnodeel123@gmail.com

<br/>

---

## 지금 하는 일

Teamcenter AWC의 선언형 프레임워크(ViewModel JSON · Service JS · HTML View)로
업무 화면을 만들고, SOA API를 붙여 데이터를 주고받습니다.

레퍼런스가 거의 없는 폐쇄적인 PLM 스택입니다.
공식 문서와 기존 코드를 읽어 동작을 역추적하는 데 시간을 많이 쓰고,
정리한 내용은 블로그에 남깁니다.

<br/>

---

## 프로젝트

### 네스트 (Nest)

**은퇴 가능 나이를 역산해서 알려주는 개인 재무 앱** &nbsp;`개인` `개발 중`

[서버](https://github.com/nowgnodeel123/retirement-planner) &nbsp;·&nbsp;
[웹](https://github.com/nowgnodeel123/retirement-planner-web)

> 자산이 지금 얼마인지 보여주는 앱은 이미 많습니다.
> 네스트는 "나는 몇 살에 은퇴할 수 있는가"에 답합니다.
> 은퇴 나이를 입력받지 않고, 후보 나이를 한 살씩 올려가며
> 목표 생활비를 90세까지 감당할 수 있는 가장 이른 나이를 찾습니다.

| | |
| :--- | :--- |
| **Backend** | Java 21 · Spring Boot 3.4.1 · PostgreSQL 16 · Flyway |
| **Frontend** | Next.js · TypeScript · Tailwind |
| **인증** | 카카오 OAuth2 · JWT |
| **배포** | Railway · Vercel |

- 주식·코인은 수량과 평단을 저장하지 않고, 매매 히스토리에서 조회 시점에 파생 계산
- 시세·환율 API(data.go.kr · Finnhub · Upbit · 한국수출입은행)가 실패해도 화면은 정상 렌더
- 국민연금 조기·연기수령, 퇴직연금 DB/DC, 연금저축 세액공제, 양도소득세 gross-up 반영

<details>
<summary><b>계산 로직 — 3구간 Gap-Filling</b></summary>

<br/>

은퇴 시점부터 90세까지를, 자산에 접근 가능해지는 시점 기준으로 세 구간으로 나눕니다.

```
은퇴 ─────────────────────────────────────────────▶ 90세
  [1. 주식/ETF만]   [2. +퇴직연금·IRP·연금저축]   [3. +국민연금]
  은퇴 ~ 55세        55세 ~ 수령개시              수령개시 ~ 90세
```

각 해에 필요한 금액에서 그 시점에 열려 있는 연금 소득을 빼고,
부족분을 주식에서 인출합니다. 이걸 은퇴 후보 나이마다 반복해
처음으로 90세까지 버티는 나이를 찾습니다.

**가장 오래 붙잡힌 부분은 금액 단위였습니다.**
목표 생활비는 물가상승률만큼 커지는 명목 금액인데
자산에만 실질 수익률을 적용하면 단위가 어긋나 부족분 계산이 무의미해집니다.
전 계산을 명목 기준으로 통일했습니다.

</details>

**남은 작업** — 배당·입금 API, 은퇴 시뮬레이터 패키지 구조 정리

<br/>

### 아힘모약 (AhHimMoYak)

**기업 직무교육 LMS · CMS 플랫폼** &nbsp;`7인 팀` `2024.10 ~ 12`

[서버](https://github.com/AhHimMoYak/lms_be) &nbsp;·&nbsp;
[웹](https://github.com/AhHimMoYak/lms_fe) &nbsp;·&nbsp;
[시연 영상](https://youtu.be/5h6VI5sSYKE)

> 메가존클라우드 Java 기반 SaaS 개발자 양성 과정 최종 프로젝트.
> **2024 부산디지털혁신아카데미 해커톤(Dev-ton) 아이디어상**
>
> 전문 개발 인력을 두기 어려운 훈련기관도 교육 과정을 직접 구성할 수 있게 만드는 것이
> 목표였습니다. 집체 교육을 대체하기 위해 실시간 강의와 실시간 퀴즈를 넣었습니다.

**내가 맡은 부분** — (여기 한 줄)

<details>
<summary><b>아키텍처 — Spring Boot에서 서버리스로</b></summary>

<br/>

Spring Boot 모놀리식으로 시작해, 기능 단위로 서버리스로 떼어내며
이벤트 기반 아키텍처로 옮겼습니다.

| | |
| :--- | :--- |
| **서버리스로 분리** | 사용자 관리 · 게시판 · 데이터 시각화 · 미디어 · 콘텐츠 업로드 |
| **ECS Fargate에 유지** | 훈련기관 · 회사 · 사원 서비스 (엔티티 결합이 강해 분리 보류) |
| **사용 서비스** | Lambda · API Gateway · DynamoDB · S3 · Cognito · IVS |
| **인프라** | Serverless Framework로 IaC 작성 → CloudFormation 스택 |

인프라를 코드로 관리해 "한 번에 세팅"이 되도록 하는 게 팀의 목표였습니다.

</details>

<br/>

---

## 기술

| | |
| :--- | :--- |
| **Backend** | Java · Spring Boot · Spring Security · JPA · Flyway |
| **Frontend** | JavaScript · TypeScript · React · Next.js |
| **Database** | Oracle · PostgreSQL · MySQL · DynamoDB |
| **Cloud** | AWS (Lambda · API Gateway · S3 · ECS Fargate · Cognito) · Serverless Framework |
| **Tools** | Git · SVN · Gradle · GitHub Actions |

실무에서 매일 쓰는 것은 **Java · JavaScript · Oracle**입니다.
Spring Boot · PostgreSQL · Next.js는 개인 프로젝트에서,
AWS 서버리스는 팀 프로젝트에서 썼습니다.
