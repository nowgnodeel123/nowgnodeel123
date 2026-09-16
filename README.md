<div align="center">

# 이동원 &nbsp;·&nbsp; Dongwon Lee

**Software Engineer** &nbsp;·&nbsp; Teamcenter PLM(1년차) / Backend

[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)
[![Velog](https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)

</div>

<br>

## 🧭 About

사내 시스템 너머의 서비스를 만들고 싶어 개인 프로젝트를 이어가는 중입니다.

설계와 판단은 직접 하고, 구현은 AI 에이전트에 역할을 나눠 맡기는 방식으로 혼자 제품을 완성하고 있습니다.

<br>

## 🗂 Projects

### 네스트 (Nest)

보유 자산으로 은퇴 가능 나이를 역산하는 자산관리 웹앱

**[링크 →](https://ldw-nest.vercel.app/)** &nbsp;·&nbsp; [backend](https://github.com/nowgnodeel123/retirement-planner) &nbsp;·&nbsp; [frontend](https://github.com/nowgnodeel123/retirement-planner-web)

> 1인 개발 · 진행중

- 단일 수익률 계산은 "운 좋으면 가능"일 뿐 → 몬테카를로 1,000회로 성공 **확률**을 산출
- 외부 시세 API가 죽으면 전체가 멈추는 구조 → 서킷브레이커 + DB 스냅샷 2단 폴백
- 자산·소득은 유출되면 되돌릴 수 없는 데이터 → PII AES-256-GCM 암호화, JWT 토큰 회전
- 계획 · 분석 · 설계 · 구현 · QA로 단계를 쪼개고 AI 에이전트에 역할을 나눠 진행

`Java 21` `Spring Boot 3` `PostgreSQL` `Next.js` `TypeScript` `Railway` `Vercel`

<br>

### 아힘모약 (AhHimMoYak)

**기업 직무교육 LMS**

[backend](https://github.com/AhHimMoYak/lms_be) &nbsp;·&nbsp; [frontend](https://github.com/AhHimMoYak/lms_fe)

> 팀 6인 · 2024 Dev-ton 아이디어상

- 코스 · 커리큘럼 · 수강신청 도메인 API 개발
- 강사용 관리 화면 및 라우팅 구현
- 시험 · 퀴즈 서비스 AWS Lambda 이관 — 핸들러 13개, `serverless.yml` 작성

`Spring Boot` `JPA` `React` `AWS Lambda` `DynamoDB`

<br>

### Blinking Eyes

**졸음을 감지해 화면 밝기와 볼륨을 낮추는 Android 앱**

[repository →](https://github.com/nowgnodeel123/CapstoneDesign)

> 개인 졸업작품

- 「눈 깜빡임 인식 기반 디바이스 조절 모듈」 특허 출원 — `10-2024-0172645`
- 교내 연구회 후속 팀 결성으로 이어짐, 공동발명자 5인 중 1인
- 2024.11.27 · 출원인 동서대학교 산학협력단
