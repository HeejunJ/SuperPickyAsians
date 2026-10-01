# SuperPickyAsians — Project Site

순수 HTML / CSS / JS로 만든 SuperPickyAsians 소개 페이지예요. 포트폴리오 사이트와 같은
화이트 + 블러쉬핑크 에디토리얼 스타일이고, 빌드 과정이 없어서 GitHub Pages에 올리기만 하면 돼요.

## 파일 구성

```
index.html      메인 페이지 (소개·문제·기능 3개·서울 데이터·여행객 기능·Founding local 모집·연락처)
privacy.html    개인정보처리방침  → App Store Connect "개인정보 처리방침 URL"에 사용
terms.html      이용약관 & 커뮤니티 가이드라인 (사용자 콘텐츠 규칙, 신고 방법)
style.css       스타일 (포트폴리오 style.css 그대로 + 맨 아래 SuperPickyAsians 추가분)
script.js       모바일 메뉴, 스크롤 reveal, 맨 위로 가기 버튼 (포트폴리오와 동일)
assets/         logo.png, favicon.png
```

## GitHub Pages로 배포하기

1. GitHub에서 새 저장소 만들기 — 예: `superpickyasians`
   → 주소는 `https://<GitHub 아이디>.github.io/superpickyasians/` 가 돼요.
2. 이 폴더의 파일 전체를 푸시:

   ```bash
   cd github-page
   git init
   git add .
   git commit -m "Add SuperPickyAsians site"
   git branch -M main
   git remote add origin https://github.com/<GitHub 아이디>/superpickyasians.git
   git push -u origin main
   ```

3. 저장소 **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` / `/(root)` → Save
4. 1~2분 뒤 상단에 뜨는 주소로 접속

## App Store Connect에 넣을 주소

| 항목 | 값 |
|---|---|
| 개인정보 처리방침 URL | `https://<아이디>.github.io/superpickyasians/privacy.html` |
| 지원 URL | `https://<아이디>.github.io/superpickyasians/#contact` |
| 마케팅 URL (선택) | `https://<아이디>.github.io/superpickyasians/` |

## 수정하기

- 문구: `index.html`에서 직접 수정 (섹션마다 주석으로 구분)
- 색상: `style.css` 맨 위 `:root { ... }`
- 연락처: `pixiefitscs@gmail.com` — 여러 파일에 있으니 바꿀 땐 전체 검색으로
- 앱 출시 후: `index.html`의 "The iOS app is launching soon" 문구와 `hero`의 버튼을 App Store 링크로 교체
- 개인정보처리방침/약관은 **법률 자문을 대신하지 않는 템플릿**이에요. 출시 전에 실제 서비스와 맞는지 한 번 확인하세요.

## 로컬에서 미리보기

```bash
cd github-page
python3 -m http.server 8000
```

그 다음 `http://localhost:8000` 접속.
