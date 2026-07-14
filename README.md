# 다온시스템 홈페이지 (www.daonsysteminc.com)

모바일 친화적인 원페이지 홈페이지입니다. GitHub Pages로 무료 호스팅합니다.

## 폴더 구성

```
daonsystem/
├── index.html      ← 홈페이지 본체 (수정은 이 파일에서)
├── CNAME           ← 커스텀 도메인 설정 파일 (www.daonsysteminc.com) — 지우지 마세요
├── README.md       ← 이 안내 문서
└── assets/         ← 이미지 폴더
```

## 1단계 — 깃허브에 파일 올리기

### 방법 A. 웹에서 드래그&드롭 (가장 쉬움)

1. https://github.com/bluedaq-cloud/daonsystem 접속 후 로그인
2. **Add file → Upload files** 클릭
3. 이 폴더 안의 **모든 파일과 assets 폴더**를 통째로 드래그해서 업로드
4. 아래 **Commit changes** 버튼 클릭

### 방법 B. 명령어 (Git 설치되어 있는 경우)

```bash
git clone https://github.com/bluedaq-cloud/daonsystem.git
cd daonsystem
# 이 폴더의 파일들(index.html, CNAME, assets 등)을 여기에 복사한 뒤
git add .
git commit -m "다온시스템 홈페이지 오픈"
git push origin main
```

## 2단계 — GitHub Pages 켜기

1. https://github.com/bluedaq-cloud/daonsystem/settings/pages 접속
2. **Source**: `Deploy from a branch` 선택
3. **Branch**: `main` / 폴더 `/ (root)` 선택 → **Save**
4. 1~2분 뒤 `https://bluedaq-cloud.github.io/daonsystem/` 에서 사이트 확인 가능

## 3단계 — 도메인 연결 (www.daonsysteminc.com)

### ① GitHub 쪽 설정

1. 같은 페이지(Settings → Pages)의 **Custom domain** 칸에 `www.daonsysteminc.com` 입력 → **Save**
   (CNAME 파일이 이미 포함되어 있어 자동 인식될 수도 있습니다)

### ② 도메인 구입처(가비아·후이즈·카페24 등) DNS 설정

도메인 관리 페이지에서 아래 레코드를 추가합니다.

| 구분 | 호스트(이름) | 값 |
|------|------------|-----|
| CNAME | `www` | `bluedaq-cloud.github.io.` |
| A | `@` (루트) | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

- CNAME 하나 + A 레코드 4개 모두 등록하세요. (A 레코드는 `daonsysteminc.com` 주소로 들어와도 접속되게 해줍니다)
- DNS 반영은 보통 10분~몇 시간 걸립니다.

### ③ HTTPS 적용

DNS 반영 후 Settings → Pages 에서 **Enforce HTTPS** 체크박스를 켭니다.
(체크가 비활성화되어 있으면 인증서 발급 중이니 몇 시간 뒤 다시 시도)

## 완료 확인

- https://www.daonsysteminc.com 접속 → 홈페이지가 뜨면 성공
- 휴대폰에서도 접속해서 모바일 화면 확인

## 내용 수정하는 법

- 전화번호·이메일·주소·문구: `index.html`을 메모장/VS Code로 열어 해당 텍스트 수정 후 다시 업로드(커밋)하면 1~2분 내 반영됩니다.
- 이미지 교체: `assets/` 폴더에 같은 파일명으로 덮어쓰면 됩니다.

## 문의 안내

- 사이트의 "전화 상담", "이메일" 버튼은 각각 `tel:010-3350-2125`, `mailto:bluedaq@gmail.com` 링크로 연결되어 있습니다.
- 나중에 문의 폼(이름·연락처 입력)이 필요하면 Formspree 같은 무료 서비스로 추가할 수 있습니다.
