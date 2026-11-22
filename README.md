# nado-ham 문서

![nado-ham 표지](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C1.PNG)

[nado-ham](https://github.com/ho8566z/nado-ham) 프로젝트의 명세서와 발표 자료를 모아 둔 문서 저장소입니다. (1차 개인 프로젝트, 2026.11.07 ~ 11.12, 이후 11.21 ~ 11.22 목표 실행 캘린더 업그레이드)

코드는 [nado-ham](https://github.com/ho8566z/nado-ham) 저장소에 있고, 이 저장소에는 기획·설계 문서와 발표 자료를 둡니다.

## 프로젝트 요약

일정을 기록하고, 다음 주 일정을 매주 일요일 21:00에 텔레그램으로 받아 보며, 장기 목표를 오늘 할 수 있는 행동으로 바꿔 주는 개인 일정 관리 웹 서비스입니다. 휴대폰 화면에서도 쓸 수 있습니다.

![주제 선정 배경](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C5.PNG)

- **해결하려는 문제**: 일정을 등록해 두고도 다시 열어 보지 않으면 놓친다. 목표는 세워도 오늘 무엇을 할지 모르면 미루게 된다.
- **핵심 기능**: 주간 브리핑(텔레그램), 목표 실행 캘린더(과정 선택 → 오늘 탭 → 시각 알림 → 주말 회고), 모바일 반응형 화면
- **기술 스택**: Java 17, Spring Boot, Spring Security, JPA(쓰기)·MyBatis(동적 조회), MySQL, Thymeleaf
- **규모**: 요구사항 68 · 기능 50 · DB 테이블 9 · 자동 테스트 477개 통과
- **목적**: 취업용 포트폴리오. 단순 CRUD에서 멈추지 않고 기획·보안·완성도로 차별화

## 폴더 구성

```
excel_output/
  calendar_bot 명세서 모음.xlsx        명세서 전체(시트 13개)
  calendar_bot 명세서 요약*.xlsx       시트별 요약본(개요·요구·기능·API·테이블·WBS·트러블슈팅·결정 기록)
  excel이미지/                         엑셀 시트 캡처
ppt_output/
  nado_ham.pptx                        발표 자료(28장)
  nado-ham.pdf                         발표 자료 PDF
  nado_ham/                            슬라이드 이미지(슬라이드1~28.PNG)
  캡처/                                실제 화면 캡처
images/ppt/                            이전 README에서 쓰던 슬라이드 이미지
```

## 명세서 (excel_output/calendar_bot 명세서 모음.xlsx)

| 시트 | 내용 |
| --- | --- |
| 프로젝트 산출물 가이드 | 제출해야 할 산출물 항목과 작성 상태 |
| 프로젝트 개요 | 서비스 목표, 권한 등급, 서비스 구성, 기술 스택, 실행 흐름, 구현 상태, 확정·미정 항목 |
| 결정 기록 | 방향·기술·설계 결정과 검토한 선택지, 이유 |
| 요구 명세서 | 구분별 요구사항(ID, 권한, 세부 기능 요구사항) |
| 기능 목록 | 기능 ID, 설명, 관련 요구사항, 액터, 우선순위, 개발 구분(기존·개선·신규) |
| 기능 명세서 | 핵심 기능의 사전 조건, 입력, 처리 순서, 업무 규칙, 예외 |
| API 명세서 | 구분, Method, URI, 권한, 구현·계획 상태 |
| 화면 기능 명세서 | 화면 ID별 영역·요소·사용자 동작·처리 규칙 |
| 테이블 명세서 | MySQL 테이블과 컬럼(`USER_MEMBER`, `PLAN`, `BRIEF_LOG`, `TELEGRAM_LINK`, `LOGIN_LOCK`, 목표 테이블 등) |
| WBS | 1차 6일 일정과 업그레이드(11/21~22) 작업별 상태 |
| 트러블슈팅 | 점검에서 찾은 문제, 영향도, 재현 방법, 처리 상태 |
| 설정·규약 | 포트, 환경변수, 구현 순서 등 개발 공통 기준 |
| 2순위 기능 | 핵심 기능을 끝낸 뒤 구현할 기능과 2순위로 둔 이유 |

## 발표 자료

[PPTX](ppt_output/nado_ham.pptx) · [PDF](ppt_output/nado-ham.pdf) — 28장, PART 1 기획 · PART 2 설계·개발 · PART 3 구현·마무리

### PART 1. 기획

| | |
| --- | --- |
| ![표지](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C1.PNG) | ![목차](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C2.PNG) |
| 표지 | 목차 |
| ![프로젝트 소개](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C3.PNG) | ![담당 범위와 규모 (요구 68 · 기능 50 · 테이블 9 · 테스트 477)](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C4.PNG) |
| 프로젝트 소개 | 담당 범위와 규모 (요구 68 · 기능 50 · 테이블 9 · 테스트 477) |
| ![주제 선정 배경 · 기획 의도](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C5.PNG) | ![유사 서비스 분석 · 차별화 포인트](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C6.PNG) |
| 주제 선정 배경 · 기획 의도 | 유사 서비스 분석 · 차별화 포인트 |
| ![핵심 사용자 시나리오](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C7.PNG) | ![개발 환경](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C8.PNG) |
| 핵심 사용자 시나리오 | 개발 환경 |
| ![활용 방안 · 기대 효과](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C9.PNG) |  |
| 활용 방안 · 기대 효과 |  |

### PART 2. 설계

| | |
| --- | --- |
| ![수행 절차 · WBS](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C10.PNG) | ![유스케이스 다이어그램](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C11.PNG) |
| 수행 절차 · WBS | 유스케이스 다이어그램 |
| ![시스템 구성도](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C12.PNG) | ![권한 등급과 접근 범위](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C13.PNG) |
| 시스템 구성도 | 권한 등급과 접근 범위 |
| ![DB 테이블 구조 (DB_CALENDAR)](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C14.PNG) | ![목표 실행 캘린더 · 흐름과 정책](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C15.PNG) |
| DB 테이블 구조 (DB_CALENDAR) | 목표 실행 캘린더 · 흐름과 정책 |

### PART 3. 구현 · 마무리

| | |
| --- | --- |
| ![핵심 구현 ① 주간 브리핑](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C16.PNG) | ![핵심 구현 ② 연동 코드와 롱 폴링](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C17.PNG) |
| 핵심 구현 ① 주간 브리핑 | 핵심 구현 ② 연동 코드와 롱 폴링 |
| ![핵심 구현 ③ 보안](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C18.PNG) | ![핵심 구현 ④ JPA · MyBatis 역할 분리](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C19.PNG) |
| 핵심 구현 ③ 보안 | 핵심 구현 ④ JPA · MyBatis 역할 분리 |
| ![핵심 구현 ⑤ 모바일 화면 대응](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C20.PNG) | ![핵심 구현 ⑥ 긴 과정 계획](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C21.PNG) |
| 핵심 구현 ⑤ 모바일 화면 대응 | 핵심 구현 ⑥ 긴 과정 계획 |
| ![핵심 구현 ⑦ 주간 보기 · 이동 · 내보내기](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C22.PNG) | ![구현 화면 ① 월간 달력 · 검색 · 통계](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C23.PNG) |
| 핵심 구현 ⑦ 주간 보기 · 이동 · 내보내기 | 구현 화면 ① 월간 달력 · 검색 · 통계 |
| ![구현 화면 ② 목표 실행](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C24.PNG) | ![구현 화면 ③ 주간 보기](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C25.PNG) |
| 구현 화면 ② 목표 실행 | 구현 화면 ③ 주간 보기 |
| ![시연 시나리오](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C26.PNG) | ![트러블슈팅 3건](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C27.PNG) |
| 시연 시나리오 | 트러블슈팅 3건 |
| ![프로젝트 평가 (구현한 것 · 한계 · 다음 단계)](ppt_output/nado_ham/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%93%9C28.PNG) |  |
| 프로젝트 평가 (구현한 것 · 한계 · 다음 단계) |  |

## 주요 결정

- 일정 관리 주제를 유지하고, 학원에서 배운 기술 범위 안에서만 사용
- 쓰기·단순 조회는 JPA, 검색·통계 같은 동적 조회는 MyBatis로 역할 분리
- 주간 브리핑과 목표 알림은 텔레그램 전용, 연동은 1회용 코드 + 롱 폴링, 알림은 환경변수로 켜는 기본 꺼짐
- 통계는 외부 차트 라이브러리 없이 표와 CSS 막대로 구현
- 모바일은 반응형 웹으로만 진행, 경계 폭 768px

결정의 이유와 검토한 선택지는 명세서의 `결정 기록` 시트에 있습니다.

## 작성자

이윤호 (개인 프로젝트)
