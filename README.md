# 박현민 · PARK HYEONMIN

백엔드를 공부하며, **요청과 응답 사이의 일을 구현합니다.**

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com/?font=Fira+Code&amp;size=21&amp;duration=2100&amp;pause=1700&amp;color=9CC9C1&amp;vCenter=true&amp;width=430&amp;height=40&amp;lines=%3E+build+%2F+verify+%2F+explain" />
  <img alt="build / verify / explain 타이핑 애니메이션" src="https://readme-typing-svg.demolab.com/?font=Fira+Code&amp;size=21&amp;duration=2100&amp;pause=1700&amp;color=356B67&amp;vCenter=true&amp;width=430&amp;height=40&amp;lines=%3E+build+%2F+verify+%2F+explain" />
</picture>

Java·Spring Boot와 TypeScript·Express로 API를 구현했습니다.
최근에는 AI 서비스를 연결하면서 응답 검증, 오류 처리, 저장된 결과의 일치 여부를 고민하고 있습니다.

---

## Projects

### 01 · ONCARE SCHEDULE

**방문요양 서비스 · 팀 프로젝트**

`Java` `Spring Boot` `JPA` `MySQL` `Gemini API`

방문요양 후기의 감정을 분석하고, 관리자가 결과를 확인할 수 있는 백엔드 기능을 구현했습니다.

| 고민한 문제 | 구현한 방식 |
|:--|:--|
| 같은 후기를 조회할 때마다 AI를 다시 호출하면 비용과 응답 시간이 늘어납니다. | 후기 내용의 해시값이 같고 저장된 분류가 유효하면 기존 결과를 재사용했습니다. |
| 후기가 수정되면 이전 분석 결과가 현재 내용과 달라집니다. | 내용이 바뀌었을 때 다시 분석하고 결과를 저장하도록 했습니다. |
| AI 응답이 예상하지 못한 분류를 반환할 수 있습니다. | 허용한 다섯 가지 감정 분류만 검증해 저장하고, 별점과 감정 방향이 다르면 따로 표시했습니다. |

[프로젝트 저장소](https://github.com/limjunhee/oncare_backend) · [후기 감정 분석 코드](https://github.com/limjunhee/oncare_backend/blob/main/src/main/java/oncare_backend/service/ReviewSentimentService.java)

### 02 · AI STUDY INDEXER

**학습 자료를 활용한 AI 학습 서비스 · 팀 졸업작품**

`TypeScript` `Express` `PostgreSQL` `JWT` `AI API`

학습 자료를 바탕으로 요약, 퀴즈, 플래시카드와 학습 리포트를 제공하는 서비스입니다. 회원가입·로그인과 JWT 인증, 사용자·과목 관리 API, AI 콘텐츠 생성 API의 백엔드 연동을 담당했습니다.

외부 AI 응답이 지연되거나 실패할 수 있어, 일부 생성 경로에서 정상 생성과 대체 처리 여부를 구분하도록 했습니다. `aiUsed`, `fallbackUsed`, `aiUrlConfigured` 값으로 실제 AI가 사용됐는지 확인할 수 있습니다.

[전체 프로젝트](https://github.com/hyeon9654/studyindexerbackfront) · [인증 로직](https://github.com/hyeon9654/studyindexerbackfront/blob/main/Back/src/services/auth.service.ts) · [AI 요약 생성 로직](https://github.com/hyeon9654/studyindexerbackfront/blob/main/Back/src/services/ai/summaryAi.service.ts)

### 03 · UNMANNED EQUIPMENT RENTAL

**무인 장비 대여 시스템 · 미니 팀 프로젝트**

`Java` `JDBC` `MySQL` `MVC`

고장·파손 신고 기능을 담당했습니다. 신고 내용을 저장하는 것에 그치지 않고 장비 상태와 대여·반납 흐름에 어떻게 연결되는지 살펴보며, DAO·DTO로 DB 접근과 데이터 전달 역할을 나눴습니다.

[프로젝트 저장소](https://github.com/hyeon9654/miniproject2) · [ReportDAO.java](https://github.com/hyeon9654/miniproject2/blob/main/miniproject2/model/dao/ReportDAO.java)

---

## How I work

**입력 → 처리 → 저장 → 응답.** API를 볼 때 이 흐름을 먼저 따라갑니다.

- 입력값과 외부 서비스의 응답을 검증합니다.
- 데이터가 변경되면 저장된 결과가 여전히 유효한지 확인합니다.
- 오류가 나면 응답뿐 아니라 처리 과정과 DB에 남은 값까지 살펴봅니다.

현재는 백엔드의 큰 흐름을 이해한 상태에서, 작은 기능을 직접 설계하고 구현하는 연습을 이어가고 있습니다. 특히 예외 처리, 데이터 정합성, 테스트로 동작을 확인하는 능력을 더 키우고 있습니다.

## Stack & learning

| 프로젝트에서 사용 | 현재 배우는 중 |
|:--|:--|
| Java, Spring Boot, JPA, JDBC | Python, NumPy, Pandas, Matplotlib |
| TypeScript, Node.js, Express, React | 데이터 분석과 시각화 |
| MySQL, PostgreSQL, JWT, Git, GitHub | 테스트와 예외 처리 설계 |

## Learning records

| 저장소 | 내용 |
|:--|:--|
| [Python](https://github.com/hyeon9654/python) | 문법, 크롤링, 데이터 분석 실습 |
| [Spring Boot](https://github.com/hyeon9654/springweb) | 웹 백엔드 학습 |
| [Java Backend](https://github.com/hyeon9654/2026_BACKEND) | Java, DB, JDBC 실습 |
| [JavaScript / Frontend](https://github.com/hyeon9654/2026_FRONTEND) | HTML, CSS, JavaScript 실습 |

---

<sub>기능을 만들고, 결과를 확인하고, 구현한 이유를 설명할 수 있도록.</sub>
