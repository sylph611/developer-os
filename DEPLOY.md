# Deploy Guide — Developer OS

배포 전 과정을 순서대로 실행합니다. 예상 소요 시간: 2-3시간.

---

## 전체 배포 순서

```
1. Notion 템플릿 3개 공개
2. GitHub 저장소 공개 설정
3. Gumroad 상품 2개 등록
4. 링크 연결 및 최종 테스트
5. 런칭 콘텐츠 배포
```

---

## Step 1. Notion 템플릿 공개

`notion-publish-checklist.md`를 열고 체크리스트를 완료합니다.

완료 후 링크 3개를 여기에 기록해둡니다:

```
Tech Interview Tracker:    https://notion.so/____________
Side Project Dashboard:    https://notion.so/____________
Developer Learning Log:    https://notion.so/____________
```

---

## Step 2. GitHub 저장소 공개

### 2-1. 로컬 Git 초기화

```bash
cd /Users/sylph/WorkspacePrivate/side-hustle-developer-os
git init
git add .
git commit -m "Initial commit: Developer OS Notion template bundle"
```

### 2-2. GitHub 저장소 생성 및 푸시

GitHub 계정에서 새 저장소 생성:
- 저장소 이름: `developer-os`
- 공개 범위: Public
- README 초기화: 체크 해제 (이미 README.md 있음)
- 생성 링크: https://github.com/new

```bash
git remote add origin https://github.com/sylph611/developer-os.git
git branch -M main
git push -u origin main
```

### 2-3. GitHub 저장소 설정

GitHub 저장소 페이지에서:

```
Settings > General > Features
```
- Discussions: 켜기 (유저 Q&A 용도)
- Issues: 켜기 (버그/피처 제안 수집)
- Wiki: 끄기 (불필요)

```
저장소 메인 페이지 > About (우측 톱니바퀴)
```
- Description: `Notion template bundle for developers — Interview tracking, side project management, learning logs`
- Website: Gumroad 상품 URL 입력 (Step 3 완료 후)
- Topics: `notion`, `productivity`, `developer-tools`, `template`, `notion-template`

### 2-4. README의 플레이스홀더 링크 업데이트

`README.md`에서 다음 항목을 실제 값으로 교체합니다:
- `https://gumroad.com/l/developer-os` → 실제 Gumroad URL
- `https://github.com/sylph611/developer-os/issues` ✅ 업데이트됨
- `https://github.com/sylph611/developer-os/discussions` ✅ 업데이트됨
- `sylph611@gmail.com` ✅ 업데이트됨

```bash
# 링크 교체 후 커밋
git add README.md
git commit -m "Update links with actual URLs"
git push
```

---

## Step 3. Gumroad 상품 등록

`gumroad-setup.md`를 열고 상품 2개를 순서대로 등록합니다.

### Gumroad 계정 생성

가입: https://gumroad.com/signup
무료 플랜으로 시작 (수수료 10%, 월 구독료 없음)

### 등록 순서

1. 유료 번들 상품 먼저 생성 (Upsell 연결을 위해 먼저 필요)
2. 무료 상품 생성
3. 무료 상품에서 유료 번들로 Upsell 연결

### 완료 후 URL 기록

```
무료 상품 URL:  https://[yourhandle].gumroad.com/l/____________
유료 번들 URL:  https://[yourhandle].gumroad.com/l/____________
```

---

## Step 4. 링크 연결 및 최종 테스트

### 링크 업데이트

GitHub README의 Gumroad 링크를 실제 URL로 업데이트:

```bash
# README.md 편집 후
git add README.md
git commit -m "Add Gumroad product links"
git push
```

### 최종 테스트 순서

**무료 상품 플로우 테스트:**
```
1. 무료 상품 Gumroad 페이지 접속 (시크릿 브라우저)
2. "Get" 클릭 → 이메일 입력
3. Receipt 이메일 수신 확인 (수 분 내)
4. 이메일에서 파일 다운로드
5. TXT 파일 열기 → Notion 링크 클릭
6. "Duplicate" 클릭 → 실제 템플릿 복사 완료 확인
7. Upsell 팝업 표시 확인
```

**유료 상품 플로우 테스트:**
```
1. 유료 번들 Gumroad 페이지 접속
2. "I want this" 클릭
3. Gumroad 본인 계정으로 로그인 후 $0로 테스트 구매
   (본인 상품은 Gumroad에서 무료 구매 가능)
4. Receipt 이메일 수신 → 파일 다운로드
5. TXT 파일에서 3개 링크 모두 테스트
```

---

## Step 5. 런칭 콘텐츠 배포

각 파일의 내용을 해당 플랫폼에 순서대로 게시합니다.

### 권장 게시 순서

```
Day 1 (론칭 당일)
  09:00  twitter-thread.md → Twitter/X 스레드 게시
  10:00  Product Hunt 제출 (product-hunt-post.md 참고)
  12:00  reddit-posts.md → r/notion 먼저 게시

Day 2
  reddit-posts.md → r/SideProject 게시
  reddit-posts.md → r/learnprogramming 게시

Day 3
  reddit-posts.md → r/cscareerquestions 게시 (면접 트래커 포커스)
```

### Product Hunt 제출

https://www.producthunt.com/posts/new

`product-hunt-post.md` 파일에서:
- Tagline 복사
- Description 복사
- Topics: Productivity, Developer Tools, Notion

제출 전 확인:
- [ ] 커버 이미지 업로드 (1270 x 760px)
- [ ] 갤러리 이미지 2-3장 업로드 (각 템플릿 스크린샷)
- [ ] 제출 시간: 한국 시간 기준 오후 2시 (Product Hunt 자정 PST 기준)
- [ ] 헌터 섭외 또는 직접 제출

---

## 최종 배포 체크리스트

### Notion

- [ ] 3개 템플릿 모두 웹 공개됨
- [ ] 3개 모두 "Allow duplicate as template" ON
- [ ] 시크릿 브라우저에서 "Duplicate" 버튼 확인

### GitHub

- [ ] 저장소 Public 상태
- [ ] README.md 링크가 모두 실제 URL
- [ ] .gitignore, LICENSE 커밋됨
- [ ] About 섹션에 설명 + Gumroad URL 입력됨
- [ ] Issues, Discussions 활성화됨

### Gumroad

- [ ] 무료 상품 공개 상태 (Published)
- [ ] 유료 번들 공개 상태 (Published)
- [ ] 무료 상품에서 유료로 Upsell 연결됨
- [ ] 두 상품 모두 Receipt 이메일 설정됨
- [ ] 테스트 구매로 전체 플로우 확인됨
- [ ] 론칭 할인 쿠폰 설정됨 (해당 시)

### 콘텐츠

- [ ] Twitter 스레드 예약 또는 게시됨
- [ ] Product Hunt 제출됨
- [ ] Reddit 첫 게시물 올라감

---

## 외부 서비스 무료 플랜 한도 요약

| 서비스 | 무료 한도 | 가입 링크 |
|---|---|---|
| Gumroad | 수수료 10%, 파일 16GB/상품 | https://gumroad.com/signup |
| GitHub | 공개 저장소 무제한 | https://github.com/signup |
| Notion | 개인 무료 플랜 (블록 무제한) | https://notion.so/signup |
| Product Hunt | 무료 제출 (1회/일) | https://producthunt.com |
