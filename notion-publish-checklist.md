# Notion Template 공개 전 체크리스트

Gumroad에 링크를 올리기 전에 3개 템플릿 각각에 대해 이 체크리스트를 실행합니다.

---

## 공통 설정 (3개 템플릿 모두)

### "Allow duplicate as template" 설정

각 템플릿 페이지에서:
```
우상단 ••• (더보기) 메뉴 > Connections 아래 "Allow duplicate as template" 토글 ON
```

이 설정이 켜져 있어야 구매자가 "Duplicate" 버튼을 볼 수 있습니다.
설정 후 공유 링크로 접속해서 "Duplicate" 버튼이 보이는지 직접 확인합니다.

### 웹 공개 설정

```
우상단 Share > Publish to web > 토글 ON
```

"Allow duplicate as template"은 웹 공개가 되어야 활성화됩니다.
웹 공개 후 생성되는 링크가 Gumroad에 올릴 최종 링크입니다.

---

## Template 1: Tech Interview Tracker

### 예시 데이터 입력 확인

- [ ] LeetCode Kanban에 문제 3-5개 예시 데이터 입력됨
  - Easy 1개: "Two Sum", Solved, Review Date 설정됨
  - Medium 2개: 각각 다른 상태 (In Progress, Solved)
  - Hard 1개: Todo 상태
- [ ] Company Pipeline에 회사 2-3개 예시 입력됨
  - 각각 다른 파이프라인 단계에 위치
  - 회사명은 실제 회사명 대신 "Company A / Company B" 등 가상 이름 사용
- [ ] Problem Notes DB에 예시 노트 2개 입력됨
  - 풀이 접근법, 시간 복잡도, 다음 리뷰 날짜 포함
- [ ] Per-Company Interview Checklist에 예시 체크리스트 1개 입력됨

### 레이아웃 확인

- [ ] 모든 데이터베이스 뷰가 올바르게 표시됨 (Kanban, Table, List)
- [ ] 필터/정렬 설정이 구매자에게 직관적으로 보임
- [ ] 페이지 최상단에 간단한 사용 설명 텍스트가 있음

### 모바일 뷰 확인

Notion 모바일 앱에서 공유 링크로 접속:
- [ ] Kanban 보드가 모바일에서 스크롤 가능
- [ ] 텍스트가 잘리지 않고 읽힘
- [ ] Duplicate 버튼이 모바일에서도 표시됨

---

## Template 2: Side Project Dashboard

### 예시 데이터 입력 확인

- [ ] Sprint Kanban에 태스크 4-6개 예시 입력됨
  - To-Do / In Progress / Done / Backlog 각 칸에 분산
  - 태스크명은 실제 개발 태스크처럼 ("Add OAuth login", "Fix mobile navbar")
- [ ] Pre-Deploy Checklist에 항목이 모두 채워져 있음
  - Security, Performance, SEO 카테고리별 체크 항목
  - 일부는 체크됨, 일부는 체크 안 됨 (실제 사용 중인 것처럼)
- [ ] Feature Roadmap에 아이디어 3-4개 입력됨
  - Idea / In Progress / Shipped 상태로 분산
- [ ] Bug Tracker에 버그 2개 예시 입력됨
  - 심각도 High 1개, Low 1개

### 레이아웃 확인

- [ ] 대시보드 메인 페이지에서 하위 DB들이 한눈에 보이는 레이아웃
- [ ] 각 DB 이름과 목적이 명확히 라벨링됨
- [ ] 페이지 상단에 "이 템플릿을 사용하는 법" 설명 텍스트 있음

### 모바일 뷰 확인

- [ ] 메인 대시보드 페이지가 모바일에서 정상 표시
- [ ] 칸반 보드 스크롤 가능
- [ ] Duplicate 버튼 모바일에서 확인

---

## Template 3: Developer Learning Log

### 예시 데이터 입력 확인

- [ ] Book Notes DB에 책 2권 예시 입력됨
  - "Clean Code" 또는 "The Pragmatic Programmer" 같은 실제 기술서 사용 가능
  - 챕터 노트, 핵심 인사이트, 액션 아이템 컬럼 모두 채워짐
- [ ] Weekly Retrospective에 주간 회고 예시 1개 입력됨
  - Wins / Struggles / Next Week Goal 모두 채워짐
  - 날짜는 실제 날짜 형식으로
- [ ] TIL Log에 예시 5-7개 입력됨
  - 다양한 날짜에 분산 (실제 사용 흔적처럼)
  - "Today I learned..." 형식의 짧은 내용
- [ ] Resource Library에 리소스 3-4개 입력됨
  - 아티클, 유튜브, 강의 각 타입 포함
  - 완료/미완료 상태 혼합

### 레이아웃 확인

- [ ] 메인 페이지에서 4개 DB에 대한 네비게이션이 명확
- [ ] 각 DB의 View 옵션이 목적에 맞게 설정됨 (TIL은 날짜 내림차순 등)
- [ ] 사용 설명 텍스트 있음

### 모바일 뷰 확인

- [ ] TIL Log 갤러리/리스트 뷰 모바일 표시 확인
- [ ] Duplicate 버튼 모바일에서 확인

---

## 공유 링크 유효성 최종 테스트

3개 링크 모두 시크릿 브라우저(비로그인 상태)에서 테스트합니다.

```
Chrome > 시크릿 창 (Ctrl+Shift+N / Cmd+Shift+N)
각 링크 접속 > "Duplicate" 버튼 클릭 > Notion 로그인 화면으로 이동 확인
```

- [ ] Tech Interview Tracker 링크 시크릿 테스트 통과
- [ ] Side Project Dashboard 링크 시크릿 테스트 통과
- [ ] Developer Learning Log 링크 시크릿 테스트 통과

모든 링크가 "Duplicate" 버튼을 보여주면 Gumroad 업로드 파일에 링크를 기입합니다.

---

## 스크린샷 캡처 (README + Gumroad 커버용)

각 템플릿의 메인 뷰를 캡처합니다:

- [ ] `assets/screenshot-interview-tracker.png` — LeetCode Kanban 뷰 전체 캡처
- [ ] `assets/screenshot-project-dashboard.png` — Sprint Kanban 뷰 전체 캡처
- [ ] `assets/screenshot-learning-log.png` — TIL Log 또는 Book Notes 뷰 캡처

캡처 권장 사이즈: 브라우저 창 1440px 너비, Notion 사이드바 숨김 상태 (Cmd+\)
