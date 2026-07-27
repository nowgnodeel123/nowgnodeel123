<div align="center">

# 이동원 &nbsp;·&nbsp; Dongwon Lee

**Java · Spring Boot 백엔드 개발자**

Siemens Teamcenter AWC 환경에서 화면 커스터마이징과 SOA API 연동을 합니다.

<br/>

[![Velog](https://img.shields.io/badge/Blog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)
[![Notion](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=notion&logoColor=white)](https://www.notion.so/22d2c41c65f1808aaef7cade80995932)
[![solved.ac](https://img.shields.io/badge/solved.ac-3B82F6?style=flat-square&logo=leetcode&logoColor=white)](https://solved.ac/profile/nowgnodeel369)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)

</div>

<br/>

---

## 🔧 지금 하는 일

Teamcenter AWC의 선언형 프레임워크(ViewModel JSON · Service JS · HTML View)로
업무 화면을 만들고, SOA API를 붙여 데이터를 주고받습니다.

레퍼런스가 거의 없는 폐쇄적인 PLM 스택입니다.
공식 문서와 기존 코드를 읽어 동작을 역추적하는 데 시간을 많이 쓰고,
정리한 내용은 블로그에 남깁니다.

<br/>

---

## 📦 프로젝트

<table>
<tr><td width="640">

### 네스트 &nbsp;<sub>Nest</sub>

**은퇴 가능 나이를 역산해서 알려주는 개인 재무 앱** &nbsp; `개인` `개발 중`

</td></tr>
</table>

> 자산이 지금 얼마인지 보여주는 앱은 이미 많습니다.
> 네스트는 **"나는 몇 살에 은퇴할 수 있는가"** 에 답합니다.
> 은퇴 나이를 입력받지 않고, 후보 나이를 한 살씩 올려가며
> 목표 생활비를 90세까지 감당할 수 있는 가장 이른 나이를 찾습니다.

<p>
<img src="https://img.shields.io/badge/Java_21-007396?style=flat-square&logo=openjdk&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring_Boot_3.4-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL_16-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white"/>
<img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white"/>
</p>

**설계에서 고민한 것**

- 금액 단위를 **명목 기준으로 통일**했습니다. 목표 생활비는 물가상승률만큼 커지는
  명목 금액인데 자산에만 실질 수익률을 적용하면 단위가 어긋나 부족분 계산이 무의미해집니다.
  가장 오래 붙잡힌 부분입니다.
- 주식·코인은 수량과 평단을 저장하지 않고, **매매 히스토리에서 조회 시점에 파생 계산**합니다.
- 시세·환율 API(data.go.kr · Finnhub · Upbit · 한국수출입은행)가 실패해도 화면은 정상 렌더됩니다.

<details>
<summary>&nbsp;<b>계산 로직 — 3구간 Gap-Filling</b></summary>

<br/>

은퇴 시점부터 90세까지를, 자산에 접근 가능해지는 시점 기준으로 세 구간으로 나눕니다.

```
은퇴 ─────────────────────────────────────────────▶ 90세
  [1. 주식/ETF만]   [2. +퇴직연금·IRP·연금저축]   [3. +국민연금]
  은퇴 ~ 55세        55세 ~ 수령개시              수령개시 ~ 90세
```

각 해에 필요한 금액에서 그 시점에 열려 있는 연금 소득을 빼고, 부족분을 주식에서 인출합니다.
이걸 은퇴 후보 나이마다 반복해 처음으로 90세까지 버티는 나이를 찾습니다.

국민연금 조기·연기수령, 퇴직연금 DB/DC, 연금저축 세액공제,
주식 양도소득세 gross-up까지 반영했습니다.

</details>

**남은 작업** &nbsp; 배당·입금 API · 은퇴 시뮬레이터 패키지 구조 정리

[![Repo](https://img.shields.io/badge/Server-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/nowgnodeel123/retirement-planner)
[![Repo](https://img.shields.io/badge/Web-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/nowgnodeel123/retirement-planner-web)

<br/>

<table>
<tr><td width="640">

### 아힘모약 &nbsp;<sub>AhHimMoYak</sub>

**기업 직무교육 LMS · CMS 플랫폼** &nbsp; `7인 팀` `2024.10 ~ 12`

</td></tr>
</table>

> 메가존클라우드 Java 기반 SaaS 개발자 양성 과정 최종 프로젝트입니다.
> 전문 개발 인력을 두기 어려운 훈련기관도 교육 과정을 직접 구성할 수 있게 만드는 것이
> 목표였고, 집체 교육을 대체하기 위해 실시간 강의와 실시간 퀴즈를 넣었습니다.

![Award](https://img.shields.io/badge/2024_부산디지털혁신아카데미_해커톤(Dev--ton)-아이디어상-F59E0B?style=flat-square)

<p>
<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
<img src="https://img.shields.io/badge/Lambda-FF9900?style=flat-square&logo=awslambda&logoColor=white"/>
<img src="https://img.shields.io/badge/API_Gateway-FF4F8B?style=flat-square&logo=amazonapigateway&logoColor=white"/>
<img src="https://img.shields.io/badge/DynamoDB-4053D6?style=flat-square&logo=amazondynamodb&logoColor=white"/>
<img src="https://img.shields.io/badge/S3-569A31?style=flat-square&logo=amazons3&logoColor=white"/>
<img src="https://img.shields.io/badge/ECS_Fargate-FF9900?style=flat-square&logo=amazonecs&logoColor=white"/>
<img src="https://img.shields.io/badge/Cognito-DD344C?style=flat-square&logo=amazoncognito&logoColor=white"/>
<img src="https://img.shields.io/badge/Serverless-FD5750?style=flat-square&logo=serverless&logoColor=white"/>
</p>

**내가 맡은 부분** &nbsp; (여기 한 줄)

<details>
<summary>&nbsp;<b>아키텍처 — Spring Boot에서 서버리스로</b></summary>

<br/>

Spring Boot 모놀리식으로 시작해, 기능 단위로 서버리스로 떼어내며
이벤트 기반 아키텍처로 옮겼습니다.

| | |
| :--- | :--- |
| **서버리스로 분리** | 사용자 관리 · 게시판 · 데이터 시각화 · 미디어 · 콘텐츠 업로드 |
| **ECS Fargate에 유지** | 훈련기관 · 회사 · 사원 서비스 — 엔티티 결합이 강해 분리 보류 |
| **인프라** | Serverless Framework로 IaC 작성 → CloudFormation 스택 |

인프라를 코드로 관리해 "한 번에 세팅"이 되도록 하는 게 팀의 목표였습니다.

</details>

[![Repo](https://img.shields.io/badge/Server-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/AhHimMoYak/lms_be)
[![Repo](https://img.shields.io/badge/Web-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/AhHimMoYak/lms_fe)
[![Demo](https://img.shields.io/badge/시연_영상-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://youtu.be/5h6VI5sSYKE)

<br/>

---

## 🛠 기술

| | |
| :--- | :--- |
| **Backend** | <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/> <img src="https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white"/> <img src="https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white"/> |
| **Frontend** | <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/> |
| **Database** | <img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/> <img src="https://img.shields.io/badge/DynamoDB-4053D6?style=flat-square&logo=amazondynamodb&logoColor=white"/> |
| **Cloud** | <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white"/> <img src="https://img.shields.io/badge/Serverless-FD5750?style=flat-square&logo=serverless&logoColor=white"/> <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/> <img src="https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white"/> |
| **Tools** | <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/SVN-809CC9?style=flat-square&logo=subversion&logoColor=white"/> <img src="https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/> |

실무에서 매일 쓰는 것은 **Java · JavaScript · Oracle**입니다.
Spring Boot · PostgreSQL · Next.js는 개인 프로젝트에서,
AWS 서버리스는 팀 프로젝트에서 썼습니다.

<br/>

---

<div align="center">

[![solved.ac](https://mazassumnida.wtf/api/v2/generate_badge?boj=nowgnodeel369)](https://solved.ac/profile/nowgnodeel369)

</div>
