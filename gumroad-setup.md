# Gumroad Setup Guide — Developer OS

Gumroad에 상품 2개를 등록하는 단계별 가이드입니다.
가입 링크: https://gumroad.com (무료 플랜 한도: 판매 수수료 10%, 월 구독 없음)

---

## 사전 준비 체크리스트

Gumroad에 로그인하기 전에 다음을 준비합니다.

- [ ] Notion 템플릿 3개의 "공유 링크" 확보 (각 페이지에서 Share > Publish to web > Allow duplicate as template 켜기)
  - Tech Interview Tracker 공유 링크: `https://notion.so/...`
  - Side Project Dashboard 공유 링크: `https://notion.so/...`
  - Developer Learning Log 공유 링크: `https://notion.so/...`
- [ ] 커버 이미지 2장 준비 (무료 상품용, 유료 번들용) — 사이즈: 1280 x 720px
- [ ] 제품 설명 카피 준비 (`landing-page-copy.md` 파일 열어두기)
- [ ] Gumroad 계정 생성 + 프로필 사진 + Bio 입력 완료

---

## 상품 1: Tech Interview Tracker (무료 리드 마그넷)

### 1-1. 새 상품 만들기

```
Gumroad 대시보드 > Products > New Product > Digital product
```

- Name: `Tech Interview Tracker — Free Notion Template`
- Price: `$0` (무료로 설정)

### 1-2. 상품 파일 업로드

Gumroad는 링크를 직접 전달하는 디지털 상품에서 `.txt` 또는 `.pdf` 파일을 사용합니다.
Notion 링크를 담은 텍스트 파일을 업로드하는 것이 가장 간단합니다.

방법 A — TXT 파일 업로드 (권장):
1. 로컬에 `interview-tracker-link.txt` 파일 생성
2. 파일 내용:

```
Developer OS — Tech Interview Tracker

Notion Template Link:
https://notion.so/[YOUR-TEMPLATE-LINK]

Setup Instructions:
1. Click the link above.
2. Click "Duplicate" in the top-right corner of the Notion page.
3. Select your workspace.
4. Follow the Setup Checklist inside the template.

Questions? Email: sylph611@gmail.com
```

3. Gumroad Product > Content > Upload File에 해당 .txt 파일 업로드

방법 B — PDF 가이드 업로드:
- Canva 또는 Notion으로 1-2페이지 PDF 가이드 제작 후 업로드
- 첫 페이지에 Notion 링크 + QR 코드 삽입

### 1-3. 상품 설명 작성

`landing-page-copy.md`에서 다음 섹션을 복사해서 붙여넣기:
- HERO SECTION (Headline + Subheadline)
- PROBLEM SECTION
- Template 1 설명 (Tech Interview Tracker)
- FAQ SECTION

### 1-4. 커버 이미지 설정

- 권장 사이즈: 1280 x 720px (16:9)
- Canva 추천 레이아웃:
  - 배경: 진한 네이비 또는 다크 그레이 (#1a1a2e 또는 #0d0d0d)
  - 상단: "FREE" 뱃지 (노란색 또는 흰색)
  - 중앙: 템플릿 스크린샷 목업 (Notion 페이지 캡처)
  - 하단: "Tech Interview Tracker — Notion Template" 텍스트
  - 폰트: Inter 또는 Space Grotesk (개발자 감성)

### 1-5. 공개 URL 설정

```
Gumroad Product > Edit > Permalink
```
- Permalink: `developer-os-free` 또는 `interview-tracker`
- 최종 URL: `https://[yourhandle].gumroad.com/l/developer-os-free`

### 1-6. Thank You 이메일 설정

```
Product > Customize > Receipt
```

Receipt 메시지 예시:
```
Thanks for downloading Tech Interview Tracker!

Your Notion template link is in the attached file.

If you find it useful, the full Developer OS bundle (Side Project Dashboard + Developer Learning Log) is available here:
https://[yourhandle].gumroad.com/l/developer-os

Good luck with the interviews.
— sylph611
```

---

## 상품 2: Developer OS Full Bundle (유료 $39)

### 2-1. 새 상품 만들기

```
Gumroad 대시보드 > Products > New Product > Digital product
```

- Name: `Developer OS — Full Notion Bundle for Developers`
- Price: `$39`
- Suggested price 체크 해제 (고정가)

### 2-2. 상품 파일 업로드

로컬에 `developer-os-bundle-links.txt` 파일 생성:

```
Developer OS — Full Bundle

Thank you for your purchase.

--- TEMPLATE LINKS ---

1. Tech Interview Tracker
   https://notion.so/[YOUR-LINK]

2. Side Project Dashboard
   https://notion.so/[YOUR-LINK]

3. Developer Learning Log
   https://notion.so/[YOUR-LINK]

--- HOW TO USE ---

1. Click each link above.
2. Click "Duplicate" in Notion (top-right corner).
3. Select your workspace.
4. Follow the Setup Checklist inside each template.

--- UPDATES ---

Future updates will be delivered to your Gumroad email.
When a new version is available, you'll receive a link via email.

Questions? Email: sylph611@gmail.com
```

이 파일을 Gumroad Product > Content > Upload File에 업로드합니다.

### 2-3. 상품 설명 작성

`landing-page-copy.md` 전체를 복사해서 Gumroad Description에 붙여넣기.
Gumroad Description 필드는 Markdown을 지원합니다.

### 2-4. 커버 이미지 설정

- 사이즈: 1280 x 720px
- 무료 상품 커버와 다른 색상 계열 사용 (구분을 위해)
- 권장 레이아웃:
  - 배경: 그레이디언트 (보라색 계열: #6c63ff → #3d3780)
  - 상단: 3개 템플릿 아이콘 또는 스크린샷 썸네일 나열
  - 중앙: "Developer OS" 대형 텍스트
  - 하단: "$39 — One-time payment" + "3 Notion Templates"
  - 우측 상단: "LAUNCH PRICE" 뱃지

### 2-5. Upsell 연결 (무료 → 유료 업셀)

```
무료 상품 Product 편집 > Upsell
```
- "Add an upsell" 클릭
- 유료 번들 상품 선택
- Upsell 헤드라인: `Upgrade to Full Bundle — $39`
- Upsell 설명: `Get the Side Project Dashboard and Developer Learning Log. One-time payment, all future updates included.`
- Discount 옵션: 필요시 업셀 전용 10% 할인 적용 가능

### 2-6. 가격 할인 설정 (론칭 한정)

```
Product > Pricing > Add a discount
```
- 론칭 2주 한정 쿠폰: `LAUNCH` → 추가 $10 할인 ($39 → $29)
- 수량 제한: 50 uses
- 유효기간: 2026-04-02까지

### 2-7. Thank You 이메일 설정

```
Product > Customize > Receipt
```

Receipt 메시지:
```
You now have access to all three Developer OS templates.

All three Notion template links are in the file attached to this email.

What to do next:
1. Open the attached .txt file
2. Click each Notion link
3. Duplicate each template to your workspace
4. Start with whichever system you need most right now

Future updates will be delivered here — no need to do anything.

Thanks for supporting an indie developer.
— sylph611
```

---

## 두 상품 공개 후 최종 확인

```
Gumroad > Products > [상품명] > View product page
```

- [ ] 무료 상품 페이지에서 "Get" 클릭 → 파일 다운로드 정상 확인
- [ ] 유료 상품 페이지에서 테스트 구매 (Gumroad는 본인 상품 무료 구매 가능)
- [ ] 다운로드한 TXT 파일의 Notion 링크 클릭 → 템플릿 Duplicate 정상 작동 확인
- [ ] Upsell 팝업이 무료 상품 결제 후 표시되는지 확인
- [ ] Receipt 이메일이 실제로 수신되는지 확인

---

## Gumroad 무료 플랜 한도

- 월 구독료: 없음
- 판매 수수료: 10% (매 판매마다)
- 파일 업로드 한도: 상품당 16GB
- 구매자 수 제한: 없음
- 커스텀 도메인: 유료 플랜 필요 (지금은 불필요)
