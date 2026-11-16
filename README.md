<div align="center">

# 이동원 &nbsp;·&nbsp; Dongwon Lee

**Software Engineer** &nbsp;·&nbsp; Teamcenter PLM(1년~) / Backend

[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nowgnodeel123@gmail.com)
[![Velog](https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nowgnodeel123/posts)

</div>

<br>

## 🗂 Projects

### 네스트 (Nest)

**지금 자산으로 은퇴 가능 나이를 역산하는 개인 재무 웹앱**

**[서비스 →](https://ldw-nest.vercel.app/)** &nbsp;·&nbsp; backend · frontend 저장소는 비공개(요청 시 열람)

> 1인 개발 · 2026.06 ~ 2026.11 · 운영 배포

- 단일 수익률 계산은 "운 좋으면 가능"일 뿐 → 몬테카를로 1,000회로 성공 **확률**을 산출, 공통 난수로 "더 좋은 입력이 더 나쁜 답"을 내던 결함 제거
- 외부 시세 API가 죽으면 전체가 멈추는 구조 → 서킷브레이커 + 마지막 종가 스냅샷 폴백, 시세는 추정·보간하지 않음
- 동시 매도 시 커넥션 풀 교착(30초 뒤 전체 500)을 재현·해결, 멱등 키로 금융 거래 중복 기록 차단
- 자산·소득은 유출되면 되돌릴 수 없는 데이터 → PII AES-256-GCM 암호화, JWT 토큰 회전, 소유자 검증 예외 없음
- Claude Code 에이전트 12개와 승인 관문 3단계로 AI 개발 조직을 설계·운영 — 티켓 54건, 의사결정 로그 450여 건
- 테스트 1,000여 개(백엔드 544 · 프론트 487)

`Java 21` `Spring Boot 3.5` `PostgreSQL` `Next.js 16` `React 19` `TypeScript` `Railway` `Vercel`

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
