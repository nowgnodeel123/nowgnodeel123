<div align="center">

# 이동원 &nbsp;·&nbsp; Dongwon Lee

### Software Engineer

Teamcenter PLM 1년차<br>
사내 시스템 너머의 서비스를 만들고 싶어 개인 프로젝트를 이어가는 중입니다

[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)
[![Velog](https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)

</div>

<br>

---

## 네스트 (Nest)

**지금 자산으로 은퇴가 준비될까요?** — 보유 자산을 정리하고 은퇴 시점에 충분한지 역산하는 자산관리 웹앱

[**데모 바로가기 →**](https://nest-rho-six.vercel.app/) &nbsp;·&nbsp; [backend](https://github.com/nowgnodeel123/retirement-planner) &nbsp;·&nbsp; [frontend](https://github.com/nowgnodeel123/retirement-planner-web)

*1인 개발 · 핵심 기능 완성, 사용성 개선 중*

> **둘러보기용 계정** `demo@nest.app` / `demo1234` — 샘플 자산 데이터가 들어 있습니다

<img src="docs/nest-simulation.png" width="640">

- **시뮬레이션 설계** — 단일 수익률로 계산하면 "언제 은퇴 가능"이 아니라 "운 좋으면 가능"이 됩니다. 몬테카를로 1,000회 시행으로 성공 확률을 내도록 직접 설계했습니다
- **장애 격리** — 외부 시세 API 장애가 곧 서비스 장애가 되지 않도록 서킷브레이커 → DB 스냅샷 2단 폴백 구성
- **민감정보 보호** — 자산·소득 데이터 특성상 PII를 AES-256-GCM으로 암호화, OAuth2 + JWT 토큰 회전 적용

`Java 21` `Spring Boot 3` `PostgreSQL` `Next.js` `TypeScript` &nbsp;·&nbsp; Oracle Cloud + Vercel

---

## 아힘모약 (AhHimMoYak)

**기업 직무교육 LMS** — 코스 개설부터 수강·시험까지 다루는 사내 교육 플랫폼

[backend](https://github.com/AhHimMoYak/lms_be) &nbsp;·&nbsp; [frontend](https://github.com/AhHimMoYak/lms_fe)

*팀 6인 · 2024 Dev-ton 아이디어상*

<img src="docs/lms-admin.png" width="640">

- **담당 범위** — 코스 · 커리큘럼 · 수강신청 도메인 API와 강사용 관리 화면 · 라우팅
- **서버리스 전환** — 시험·퀴즈는 응시 기간에만 트래픽이 몰리는 구조라 상시 구동이 낭비였습니다. AWS Lambda로 이관하며 핸들러 13개와 `serverless.yml`을 직접 작성

`Spring Boot` `JPA` `React` `AWS Lambda` `DynamoDB`

---

## Blinking Eyes

**졸음 감지 기반 디바이스 제어 Android 앱** — 눈 깜빡임을 인식해 화면 밝기와 볼륨을 자동으로 낮춥니다

[repository →](https://github.com/nowgnodeel123/CapstoneDesign)

*개인 졸업작품 · 특허 출원* `10-2024-0172645`

<img src="docs/blinking-eyes.gif" width="280">

- **인식 로직** — 전면 카메라 프레임에서 눈 영역을 추출해 깜빡임 주기로 졸음 상태를 판정
- **성능 분리** — OpenCV 처리부를 C++ NDK/JNI로 내려 실시간 프레임 처리 부담 완화
- **특허 출원** — 이 결과물이 교내 연구회 후속 과제로 이어져 「눈 깜빡임 인식 기반 디바이스 조절 모듈」을 공동발명자(5인 중 1인)로 출원 *(2024.11.27 · 출원인 동서대학교 산학협력단)*

`Android(Java)` `C++ NDK/JNI` `OpenCV`
