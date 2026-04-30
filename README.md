# 5월 봄 여행 일정표 🌸

세종 다온숲 글램핑 가족 여행 일정표 (2026.05.02 ~ 05.03)

부모님과 가족에게 공유하기 위한 정적 HTML 페이지입니다. 봄 숲 분위기의 따뜻한 에디토리얼 디자인으로, 데스크탑과 모바일 모두에서 잘 보이도록 만들었어요.

## 미리보기

- 히어로 섹션 + 다온숲 글램핑 메인 사진
- 5월 2일 / 5월 3일 타임라인 (모든 일정마다 실제 사진)
  - 12:00 간장게장 점심 — Unsplash 해산물 사진
  - 15:00 글램핑 도착 — 다온숲 글램핑 외관
  - 저녁 캠핑 — 다온숲 야경
  - 11:00 체크아웃 — 다온숲 자연
  - 오후 대전 아울렛 — Unsplash 쇼핑몰 인테리어
  - 21:00 귀가 — Unsplash 한국 야경 (인천 송도)
- 글램핑 사진 갤러리 (5장)
- 숙소 정보 (주소, 객실, 체크인/아웃)
- 이용 시 주의사항
- 연락처 (전화번호 클릭 시 통화 / 홈페이지 링크)

## 로컬에서 보기

브라우저에서 `index.html`을 그냥 열거나, 간단한 로컬 서버로:

```bash
python3 -m http.server 8000
# 브라우저에서 http://localhost:8000 열기
```

## GitHub Pages에 올리기

### 1. 새 레포지토리 만들기

GitHub에서 새 레포지토리를 만듭니다 (예: `spring-trip-2026`).

### 2. 파일 업로드

이 폴더의 모든 파일(`index.html`, `.nojekyll`, `README.md`)을 레포지토리 루트에 업로드:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/spring-trip-2026.git
git push -u origin main
```

### 3. GitHub Pages 활성화

레포지토리의 **Settings → Pages** 메뉴에서:

- **Source**: Deploy from a branch
- **Branch**: `main` / `/ (root)` 선택 후 **Save** 클릭

1~2분 후 `https://YOUR_USERNAME.github.io/spring-trip-2026/` 에서 공개됩니다.

## 사진 출처 및 라이선스

이 페이지의 모든 사진은 외부 HTTPS CDN에서 hotlink로 불러옵니다. 직접 호스팅하지 않으므로 레포 용량은 매우 작아요.

### 다온숲 사진 (글램핑 관련 6장)

- 출처: [daonsup.com](http://daonsup.com)
- 전송 방식: [wsrv.nl](https://wsrv.nl) HTTPS 이미지 프록시 사용
- 이유: 다온숲 사이트가 HTTP 프로토콜이라 GitHub Pages(HTTPS)에서 직접 로드 시 mixed-content로 차단됨. wsrv.nl이 HTTPS로 재전송하고 자동 최적화도 해줍니다.

### Unsplash 사진 (3장)

| 장소 | 사진가 |
|---|---|
| 간장게장 | [Frank Zhang](https://unsplash.com/@frankzphoto) |
| 대전 아울렛 | [WeLoveBarcelona.de](https://unsplash.com/@welovebarcelona) |
| 귀가 (송도 야경) | [Daesun Kim](https://unsplash.com/@lifeandyouth) |

[Unsplash License](https://unsplash.com/license)에 따라 상업적/비상업적 자유 이용이 가능하고, 출처 표기는 의무가 아니지만 권장됩니다.

## 직접 찍은 사진으로 교체하고 싶다면

여행 다녀온 후 실제 가족 사진으로 교체하는 것을 강력 추천해요.

1. 레포지토리에 `images/` 폴더를 만들고 사진을 넣습니다
2. `index.html`에서 해당 `<img>` 태그의 `src` 값을 로컬 경로로 변경

```html
<!-- 변경 전 (Unsplash) -->
<img src="https://images.unsplash.com/photo-1556906851-99df9cb88ad2?..." alt="간장게장">

<!-- 변경 후 (로컬 사진) -->
<img src="images/lunch-crab.jpg" alt="간장게장">
```

## 파일 구성

```
spring-trip-2026/
├── index.html      # 일정표 페이지 (단일 파일, 모든 스타일 포함)
├── .nojekyll       # GitHub Pages Jekyll 빌드 우회
└── README.md       # 이 문서
```

## 사용 폰트

- **Gowun Batang** / **Gowun Dodum** (한글) — Google Fonts, SIL Open Font License
- **Cormorant Garamond** (영문 액센트) — Google Fonts, SIL Open Font License

## 라이선스

개인 가족 여행용으로 만든 페이지입니다. 자유롭게 수정해서 사용하세요.
