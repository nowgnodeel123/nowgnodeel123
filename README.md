<div align="center">

# 이동원 &nbsp;·&nbsp; Dongwon Lee

**Software Engineer** &nbsp;|&nbsp; Java · Spring Boot · Teamcenter

[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)
[![Velog](https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)

</div>

<br>

## About

Java · Spring Boot 백엔드를 중심으로 개발합니다. 코드를 고치기 전에 전제부터 의심하는 편입니다.

SI 소속으로 대기업 사업장에 파견되어 **Siemens Teamcenter(PLM) 커스터마이징과 데이터 마이그레이션**을 맡고 있습니다.
431만 건 대상 배치를 재설계해 성공률을 81.5%로 안정화했고, 화면 검색값과 193만 건 차이가 나던 이관 쿼리를
조건 단위로 검증해 확정했습니다. 사내 코드는 공개할 수 없어, 테이블 · 컬럼명을 익명화해 그 과정을 기록합니다 →
**[velog.io/@nowgnodeel123](https://velog.io/@nowgnodeel123/posts)**

개인 프로젝트 **네스트**는 요구사항 분석 · 설계 · 개발 · QA · 배포 전 단계를 Claude Code 기반 워크플로우로 진행하고 있습니다.
각 단계의 역할과 지침을 직접 정의했고, 도메인 설계와 은퇴 시뮬레이션 계산 로직, 인증 · 보안 · 외부 API 장애 대응 방식은
제가 판단해 결정했습니다. 커밋에 의사결정 번호(`D-###`)와 마일스톤(`M##`)을 붙여 근거를 남깁니다.

<br>

## Projects

### 네스트 (Nest) &nbsp;·&nbsp; [backend →](https://github.com/nowgnodeel123/retirement-planner) &nbsp;/&nbsp; [frontend →](https://github.com/nowgnodeel123/retirement-planner-web)

보유 자산으로 은퇴 가능 나이를 역산하는 자산관리 웹앱 · 1인 개발 · 진행중

- 도메인 설계와 은퇴 시뮬레이션 계산 로직 직접 설계 — 몬테카를로 성공률 1,000회 시행
- 인증 · 보안 — OAuth2(카카오), JWT 리프레시 토큰 회전(RTR), 사용자 PII AES-256-GCM 암호화, 자산 변경 감사 로그
- 외부 시세 API 장애 대응 — Resilience4j 서킷브레이커 + DB 스냅샷까지 2단 폴백, 기준 시점을 값과 함께 응답
- 미인증 API 요청을 302 리다이렉트 대신 401로 응답하도록 변경 (프론트가 인증 만료와 네트워크 장애를 구분하지 못하던 문제)
- `Java 21` `Spring Boot 3` `PostgreSQL` `Flyway` `Next.js` `TypeScript` · Oracle Cloud + Vercel 배포

### 아힘모약 (AhHimMoYak) &nbsp;·&nbsp; [backend →](https://github.com/AhHimMoYak/lms_be) &nbsp;/&nbsp; [frontend →](https://github.com/AhHimMoYak/lms_fe)

기업 대상 직무교육 LMS · 팀 6인 · 본인 참여 2024.08 ~ 2024.12

- 2024 부산디지털혁신아카데미 Dev-ton **아이디어상** 수상
- **코스 · 커리큘럼 도메인(BE)** — 강사 대시보드 코스 리스트, 카테고리별 페이징 조회,
  커리큘럼 생성 · 수정 · 삭제, 비로그인 코스 상세 조회
- **수강신청 도메인(BE)** — 요청 → 승인/거절 응답 → 요청 내역 조회 흐름 전체 구현.
  `Affiliation` · `User` 연관관계 수정, 실제 의미와 맞지 않던 `Contract` → `CourseProvide` 네이밍 정리
- **강사용 관리 화면 및 라우팅(FE)** — 코스 · 커리큘럼 생성/수정 페이지, 라이브 방송 생성, 미디어 업로드,
  코스 상세 페이지 구현 및 `Render.jsx` 라우팅 구성
- **시험 · 퀴즈 서비스 서버리스 이관** — 팀 차원 AWS 전환 중 담당 서비스 이관을 직접 수행.
  퀴즈 단위로 만든 기능을 시험 단위로 재정의하고 기능별 람다로 분리(핸들러 13개),
  담당 서비스 `serverless.yml` 작성, DynamoDB 테이블 및 ContentType 정의
- `Spring Boot` `JPA` `React` `AWS Lambda` `API Gateway` `DynamoDB` `S3`

### Blinking Eyes &nbsp;·&nbsp; [repository →](https://github.com/nowgnodeel123/CapstoneDesign)

눈 감지로 졸음을 판단해 화면 밝기와 볼륨을 낮추는 Android 앱 · 개인 졸업작품

- 눈 미검출 2초 → 10초간 10단계로 밝기 · 볼륨 감소 → 5초 후 종료
- 배터리 소모를 줄이기 위해 카메라를 120초 주기 20초만 활성화
- 완성 후 알려진 이슈 6건을 직접 진단해 README에 기록
- **이 작업을 기반으로 지도교수가 이끄는 교내 연구회에서 후속 팀이 구성되어
  「눈 깜빡임 인식 기반 디바이스 조절 모듈」 특허 출원**
  <br>출원 2024.11.27 (`10-2024-0172645`) · 공개 2026.06.04 (`10-2026-0081971`)
  <br>출원인 동서대학교 산학협력단 · 공동발명자 5인 중 1인 · 과기정통부 SW중심대학 사업
- `Android(Java)` `C++ NDK/JNI` `OpenCV`

<br>

## Tech Stack

| | |
| :--- | :--- |
| **Language** | ![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=OpenJDK&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) |
| **Framework** | ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) |
| **Database** | ![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **Cloud** | ![AWS Lambda](https://img.shields.io/badge/AWS_Lambda-FF9900?style=flat-square&logo=awslambda&logoColor=white) ![API Gateway](https://img.shields.io/badge/API_Gateway-FF4F8B?style=flat-square&logo=amazonapigateway&logoColor=white) ![DynamoDB](https://img.shields.io/badge/DynamoDB-4053D6?style=flat-square&logo=amazondynamodb&logoColor=white) ![S3](https://img.shields.io/badge/S3-569A31?style=flat-square&logo=amazons3&logoColor=white) |
| **Deployment** | ![Oracle Cloud](https://img.shields.io/badge/Oracle_Cloud-C74634?style=flat-square&logo=oracle&logoColor=white) ![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white) |
| **실무 도메인** | ![Teamcenter AWC](https://img.shields.io/badge/Teamcenter_AWC-009999?style=flat-square&logo=siemens&logoColor=white) ![SOA API](https://img.shields.io/badge/SOA_API-006E6E?style=flat-square) |
