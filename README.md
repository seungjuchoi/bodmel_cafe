# 봄들 카페 - 정적 웹사이트

신라호텔 셰프가 운영하는 프리미엄 디저트 카페의 홍보 페이지입니다.

## 주요 기능

- 신라호텔 셰프 경력을 강조한 브랜드 스토리
- 시그니처 메뉴 소개
- 반응형 디자인 (모바일 최적화)
- 쇼핑몰 및 인스타그램 연동 준비

## Cloudflare Pages 배포 방법

### 1. Git 저장소 설정
```bash
# 현재 디렉토리에서 Git 초기화
git init

# 파일 추가
git add .

# 첫 번째 커밋
git commit -m "Initial commit: 봄들 카페 정적 웹사이트"

# GitHub 저장소에 푸시 (GitHub에서 새 저장소 생성 후)
git remote add origin https://github.com/your-username/bodmel-cafe.git
git branch -M main
git push -u origin main
```

### 2. Cloudflare Pages 설정

1. **Cloudflare 대시보드 접속**
   - [Cloudflare Dashboard](https://dash.cloudflare.com/)에 로그인
   - 좌측 메뉴에서 "Pages" 선택

2. **새 프로젝트 생성**
   - "Create a project" 클릭
   - "Connect to Git" 선택
   - GitHub 저장소 연결

3. **빌드 설정**
   - Project name: `bodmel-cafe` (또는 원하는 이름)
   - Production branch: `main`
   - Build command: (비워두기 - 정적 파일)
   - Build output directory: `/` (루트 디렉토리)

4. **배포 완료**
   - 배포가 완료되면 `https://bodmel-cafe.pages.dev` 형태의 URL 제공
   - 커스텀 도메인 연결 가능

### 3. 커스텀 도메인 설정 (선택사항)

1. Cloudflare Pages 대시보드에서 프로젝트 선택
2. "Custom domains" 탭 클릭
3. "Set up a custom domain" 클릭
4. 도메인 입력 및 DNS 설정 완료

## 업데이트 방법

파일을 수정한 후 Git으로 푸시하면 자동으로 재배포됩니다:

```bash
git add .
git commit -m "업데이트 내용"
git push
```

## 연락처 정보 업데이트

`index.html` 파일의 다음 섹션을 실제 정보로 업데이트하세요:

- 전화번호: 02-1234-5678
- 주소: 서울특별시 강남구 논현동 123-45
- 쇼핑몰 링크: `href="#"` 부분을 실제 URL로 변경
- 인스타그램 링크: `href="#"` 부분을 실제 URL로 변경

## 파일 구조

```
bodmel_statid_page/
├── index.html          # 메인 페이지
├── styles.css          # 스타일시트
└── README.md           # 이 파일
```