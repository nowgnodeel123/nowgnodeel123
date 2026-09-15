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

<br>

### 네스트 (Nest)

보유 자산으로 은퇴 가능 나이를 역산하는 자산관리 웹앱

**[데모 →](https://nest-rho-six.vercel.app/)** &nbsp;·&nbsp; [backend](https://github.com/nowgnodeel123/retirement-planner) &nbsp;·&nbsp; [frontend](https://github.com/nowgnodeel123/retirement-planner-web)

> 1인 개발 · 진행중
> `Java 21` `Spring Boot 3` `PostgreSQL` `Next.js` `TypeScript` `Oracle Cloud` `Vercel`

**시뮬레이션 설계**
은퇴 시점 계산 로직을 직접 설계. 몬테카를로 1,000회 시행으로 성공률 산출

**장애 격리**
외부 시세 API에 서킷브레이커 적용, DB 스냅샷까지 2단 폴백 구성

**민감정보 보호**
PII AES-256-GCM 암호화, OAuth2 · JWT 토큰 회전 적용

**개발 프로세스 설계**
분석 · 설계 등 단계마다 AI 에이전트에 역할을 부여하고, 한 단계가 끝나면 그 산출물을 다음 단계로 넘기는 방식으로 진행. 컨텍스트 주입에는 MCP를 활용

<br>

### 아힘모약 (AhHimMoYak)

기업 직무교육 LMS

[backend](https://github.com/AhHimMoYak/lms_be) &nbsp;·&nbsp; [frontend](https://github.com/AhHimMoYak/lms_fe)

> 팀 6인 · 2024 Dev-ton 아이디어상
> `Spring Boot` `JPA` `React` `AWS Lambda` `DynamoDB`

**담당 범위**
코스 · 커리큘럼 · 수강신청 도메인 API와 강사용 관리 화면 · 라우팅

**서버리스 전환**
시험 · 퀴즈 서비스를 AWS Lambda로 이관 (핸들러 13개, `serverless.yml` 작성)

<br>

### Blinking Eyes

졸음을 감지해 화면 밝기와 볼륨을 낮추는 Android 앱

[repository →](https://github.com/nowgnodeel123/CapstoneDesign)

> 개인 졸업작품
> `Android(Java)` `C++ NDK/JNI` `OpenCV`

**특허 출원** &nbsp;`10-2024-0172645`
이 작업을 기반으로 교내 연구회 후속 팀이 구성되어 「눈 깜빡임 인식 기반 디바이스 조절 모듈」 출원
공동발명자 5인 중 1인 · 2024.11.27 · 출원인 동서대학교 산학협력단
