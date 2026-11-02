
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:0f766e&height=210&section=header&text=Park%20Hyeonmin&fontSize=50&fontColor=ffffff&animation=fadeIn&desc=Backend%20%2F%20AI%20Integration&descSize=20&descAlignY=65" width="100%" alt="Park Hyeonmin - Backend Developer" />

### 👨‍💻 백엔드 개발을 중심으로 AI 서비스 연동까지 경험한 개발자

동작하는 기능을 넘어, **데이터 흐름과 예외 상황을 설명할 수 있는 코드**를 지향합니다.

Java · Spring Boot와 TypeScript · Express를 활용해 REST API를 구현하고,  
데이터베이스와 외부 AI 서비스가 연결되는 과정을 개발·검증해 왔습니다.

[![Repositories](https://img.shields.io/badge/GitHub-Projects-181717?style=for-the-badge&logo=github)](https://github.com/hyeon9654?tab=repositories)
[![Graduation Project](https://img.shields.io/badge/Graduation-AI_Study_Indexer-0F766E?style=for-the-badge)](https://github.com/hyeon9654/studyindexerbackfront)
[![Team Project](https://img.shields.io/badge/Team-ONCARE_SCHEDULE-2563EB?style=for-the-badge)](https://github.com/limjunhee/oncare_backend)

</div>

---

## 👋 About Me

- 🎯 **목표 직무** : 백엔드 개발자 / 풀스택 개발자
- 🧩 **개발 경험** : Java, Spring Boot, TypeScript, Node.js, Express, React
- 🗄️ **데이터베이스** : MySQL, PostgreSQL
- 🤖 **AI 연동 경험** : Gemini API, 외부 AI 서버 연동, AI 응답 검증 및 대체 처리
- 📚 **현재 학습** : Python, NumPy, Pandas, 데이터 분석 및 시각화

> 팀 프로젝트에서는 **개인 담당 기능과 팀 전체 구현 범위를 구분하여 기록**합니다.

---

## 🛠 Tech Stack

### 프로젝트에서 사용한 기술

<div align="center">

<img src="https://skillicons.dev/icons?i=java,spring,ts,nodejs,express,postgres,mysql,js,react,html,css,git,github&perline=7" />

</div>

### 학습 및 실습 중인 기술

<div align="center">

<img src="https://skillicons.dev/icons?i=py" />

**NumPy · Pandas · Matplotlib · Seaborn**

</div>

---

## 🚀 Featured Projects

### 🎓 01. AI Study Indexer

**AI 기반 개인 맞춤형 학습 지원 서비스**

`TypeScript` `Node.js` `Express` `PostgreSQL` `JWT` `React` `AI API`

대학생의 학습 자료를 기반으로 요약, 퀴즈, 플래시카드, 학습 리포트 등을 제공하는 팀 졸업작품입니다.

**담당 역할 : 백엔드 개발 중심**

- JWT 기반 회원가입 및 로그인 API 구현
- 사용자 정보 조회 및 과목 관리 CRUD 구현
- Router → Controller → Service → Repository 계층 구조 활용
- AI 학습 콘텐츠 생성 API의 백엔드 연동 및 결과 저장 흐름 검증
- AI 응답 실패 상황을 고려한 Fallback 처리 및 응답 메타데이터 검증 참여

**핵심 기술 포인트**

| 구분 | 구현 및 검증 내용 |
|---|---|
| 인증 | JWT 기반 사용자 식별 및 API 접근 검증 |
| 데이터 관리 | PostgreSQL을 통한 사용자·과목·학습 데이터 처리 |
| 아키텍처 | Controller / Service / Repository 역할 분리 |
| AI 연동 | 백엔드가 AI 서버를 호출하고 결과를 DB에 저장하는 구조 |
| 장애 대응 | AI 사용 여부와 Fallback 사용 여부를 응답에 구분 |

**🔗 프로젝트 및 실제 코드**

- [통합 프로젝트 저장소](https://github.com/hyeon9654/studyindexerbackfront)
- [인증 서비스 구현 코드](https://github.com/hyeon9654/studyindexerbackfront/blob/main/Back/src/services/auth.service.ts)
- [AI 연동 서비스 코드](https://github.com/hyeon9654/studyindexerbackfront/tree/main/Back/src/services/ai)

---

### 🏥 02. ONCARE SCHEDULE

**방문요양 일정 및 요양보호사 관리 플랫폼**

`Java` `Spring Boot` `JPA` `MySQL` `React` `Gemini API`

방문요양센터의 일정 관리와 요양보호사 관리 업무를 지원하는 국비교육 팀 프로젝트입니다.

**담당 역할 : 백엔드 API 및 AI 후기 분석**

- 요양보호사 관리 API
- 근무 가능 시간 관리 API
- 후기 등록·조회·수정·삭제 API
- Gemini API를 활용한 후기 감정 5단계 분류
- 분석 결과 DB 저장 및 기존 결과 재사용
- 후기 별점과 감정 분석 결과의 불일치 감지

**핵심 트러블슈팅 : 동일한 후기의 AI 중복 호출**

**문제**

이미 분석한 후기 내용을 다시 분석할 경우 불필요한 외부 API 호출이 발생할 수 있었습니다.

**해결**

후기 내용의 해시값을 저장하고 기존 분석 결과와 비교하도록 구성했습니다.

후기 내용이 같고 기존 감정 분류가 유효하면 저장된 분석 결과를 반환하고, 내용이 변경되면 재분석하도록 처리했습니다.

**추가 검증**

- AI의 응답을 정해진 5개 감정 분류에 속하는지 검증
- 별점과 텍스트 감정 결과의 불일치 여부를 별도로 표시
- 후기 분석 통계는 저장된 결과를 기준으로 계산

**🔗 프로젝트 및 실제 코드**

- [ONCARE 팀 백엔드](https://github.com/limjunhee/oncare_backend)
- [후기 감정 분석 서비스 구현 코드](https://github.com/limjunhee/oncare_backend/blob/main/src/main/java/oncare_backend/service/ReviewSentimentService.java)
- [ONCARE 팀 프론트엔드](https://github.com/limjunhee/oncare_frontend)

---

### 🔐 03. 무인 장비 대여 시스템

**Java 기반 장비 대여 및 관리 프로그램**

`Java` `JDBC` `MySQL` `MVC`

국비교육 팀 미니프로젝트로, 콘솔 환경에서 장비와 보관함을 관리하는 프로그램입니다.

**담당 역할 : 고장·파손 신고**

- 장비 이상 상태 신고 기능 구현
- JDBC를 통한 데이터베이스 연동
- DAO / DTO / View 기반 MVC 구조 활용
- 팀원별 기능 구현 및 Git 협업

**🔗 프로젝트 및 실제 코드**

- [프로젝트 저장소](https://github.com/hyeon9654/miniproject2)
- [고장·파손 신고 DAO](https://github.com/hyeon9654/miniproject2/blob/main/miniproject2/model/dao/ReportDAO.java)

---

## 🧭 Development Approach

**요구사항 이해 → 데이터 구조 설계 → API 구현 → 예외 처리 → 기능 검증**

개발 과정에서 중요하게 생각하는 부분은 다음과 같습니다.

1. API 요청이 어떤 계층을 거쳐 DB까지 전달되는지 이해하기
2. 입력값 검증과 예외 상황을 고려하기
3. 외부 API의 응답을 그대로 신뢰하지 않고 검증하기
4. 중복 처리와 불필요한 호출을 줄이기
5. 자신이 구현한 기능의 동작 원리와 한계를 설명하기

---

## 📚 Learning & Practice

| 분야 | 학습 내용 | GitHub |
|---|---|---|
| Java / Spring Boot | REST API, JPA, MySQL, 웹 개발 | [Spring Boot](https://github.com/hyeon9654/springweb) |
| JavaScript / HTML / CSS | DOM, 이벤트, 웹 화면 구현 | [Frontend](https://github.com/hyeon9654/2026_FRONTEND) |
| Python | 기초 문법, NumPy, Pandas, 데이터 분석 | [Python](https://github.com/hyeon9654/python) |

---

<div align="center">

### Learn → Build → Verify → Explain

**작동하는 코드를 넘어, 그 이유를 설명할 수 있는 개발자가 되겠습니다.**

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f766e,100:0f172a&height=100&section=footer" width="100%" alt="Footer" />

</div>
