# zidudu.github.io

개인 정적 사이트 모음입니다. 빌드 도구 없이 HTML/CSS/JS만 사용합니다.

## 구성

| 경로 | 설명 |
|---|---|
| `index.html` | **Website Hub**: Education / Games / History 카테고리별 링크 카드 페이지 |
| `R_S.js` | 카테고리 필터(`showCategory`)와 제목 검색(`searchLinks`) |
| `R_S.css` | Website Hub 스타일 |
| `signaldesk-test/` | **SignalDesk** 랜딩 페이지 시안 (운영 대시보드 SaaS 컨셉) |

## Website Hub

- 상단 메뉴로 카테고리를 필터링하고, 검색창에 입력하면 카드 제목으로 걸러냅니다.
- 카드 3개는 `index.html`에 하드코딩된 예시 데이터입니다 (Educational Resource 1, Game Site 1, Historical Article 1). 실제 링크는 아직 없습니다.

## SignalDesk (`signaldesk-test/`)

SaaS 제품 랜딩 페이지 시안입니다. Command Center 미리보기, 워크플로, 기능 소개, 연동 서비스 목록, 요금제(Starter/Team/Business) 섹션으로 구성됩니다.

- 표시되는 알림·고객·MRR·차트 수치는 모두 목업 데이터입니다.
- 동작하는 JS는 `View demo` 버튼(미리보기로 스크롤 + 강조)과 Tasks 탭 선택 표시뿐입니다.
- 파일: `index.html`, `signaldesk-style.css`(약 790줄), `signaldesk-script.js`

## 실행

서버 없이 `index.html`을 브라우저로 열면 됩니다. 로컬 서버가 필요하면:

```bash
python3 -m http.server 8000
```

- Website Hub: http://localhost:8000/
- SignalDesk: http://localhost:8000/signaldesk-test/

## 알려진 이슈

- `index.html`은 `styles.css`, `script.js`를 참조하지만 저장소에는 `R_S.css`, `R_S.js`만 있습니다. 이 상태로는 스타일과 JS가 로드되지 않습니다. 파일명을 맞추거나 `<link>`/`<script>` 경로를 수정해야 합니다.
- 같은 Website Hub의 다른 버전이 [`chatgpt-web`](https://github.com/zidudu/chatgpt-web)에 있습니다(List 보기 기능 포함).
