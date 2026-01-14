# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 언어 및 커뮤니케이션 규칙

- **기본 응답 언어**: 한국어
- **코드 주석**: 한국어로 작성
- **커밋 메시지**: 한국어로 작성
- **문서화**: 한국어로 작성
- **변수명/함수명**: 영어 (코드 표준 준수)

## 프로젝트 개요

개발자 웹 이력서 프로젝트로, HTML, CSS, JavaScript, Tailwind CSS를 사용하여 반응형 포트폴리오 사이트를 구축합니다.

## 기술 스택

- **HTML5**: 시맨틱 마크업
- **CSS3**: 스타일링 및 애니메이션
- **JavaScript (ES6+)**: 인터랙션 및 동적 기능
- **Tailwind CSS**: 유틸리티 기반 스타일링 (CDN 방식)

## 프로젝트 구조

```
project/
├── index.html           # 메인 HTML 파일
├── css/
│   └── style.css       # 커스텀 CSS
├── js/
│   └── main.js         # JavaScript 기능
└── images/             # 이미지 리소스
```

## 개발 명령어

이 프로젝트는 정적 HTML 사이트이므로 빌드 과정이 필요하지 않습니다.

### 로컬 개발 서버 실행

```bash
# Python 3가 설치된 경우
python -m http.server 8000

# Node.js가 설치된 경우 (npx 사용)
npx serve .
```

브라우저에서 `http://localhost:8000` 접속

### 배포

```bash
# GitHub Pages 배포 (main 브랜치 푸시)
git add .
git commit -m "커밋 메시지"
git push origin main
```

## 아키텍처 및 구조

### HTML 구조

`index.html`은 8개의 주요 섹션으로 구성됩니다:

1. **헤더 (Header)**: 네비게이션 메뉴
2. **프로필 (Profile)**: 프로필 사진, 이름, 직무, 연락처
3. **소개 (About)**: 자기소개 및 비전
4. **기술 스택 (Skills)**: 기술 목록 및 숙련도 시각화
5. **프로젝트 (Projects)**: 프로젝트 카드 그리드
6. **경력 (Experience)**: 타임라인 형식의 경력 사항
7. **학력/자격증 (Education/Certifications)**: 학력 및 자격증 정보
8. **연락처 (Contact)**: 연락 폼 및 소셜 링크

### JavaScript 기능 (js/main.js)

- **스크롤 애니메이션**: Intersection Observer API 사용
- **네비게이션 고정**: 스크롤 시 헤더 고정
- **부드러운 스크롤**: 네비게이션 클릭 시 부드러운 이동
- **폼 유효성 검사**: 연락처 폼 검증
- **다크모드**: 선택사항

### CSS 스타일링 (css/style.css)

Tailwind CSS를 CDN으로 사용하되, 커스텀 스타일은 `style.css`에 추가합니다:
- 추가 애니메이션
- Tailwind로 표현하기 어려운 복잡한 스타일
- 커스텀 컴포넌트 스타일

## 디자인 시스템

### 컬러 팔레트

```css
Primary: #3B82F6 (Blue)
Secondary: #8B5CF6 (Purple)
Accent: #10B981 (Green)
Background: #F9FAFB (Light Gray)
Text: #111827 (Dark Gray)
```

### 타이포그래피

- **헤딩**: Inter, Poppins
- **본문**: Inter, 'Noto Sans KR'
- **크기**: H1(3rem), H2(2.5rem), H3(2rem), Body(1rem)

### 반응형 브레이크포인트

```css
Mobile: < 640px
Tablet: 640px ~ 1024px
Desktop: > 1024px
```

## 코딩 컨벤션

### HTML

- 시맨틱 태그 사용 (`<section>`, `<article>`, `<nav>` 등)
- ARIA 레이블 추가로 접근성 확보
- 들여쓰기: 2칸

### CSS

- Tailwind CSS 유틸리티 클래스 우선 사용
- 커스텀 스타일은 `css/style.css`에 추가
- BEM 네이밍 사용 (커스텀 클래스)
- 들여쓰기: 2칸

### JavaScript

- ES6+ 문법 사용
- camelCase 네이밍
- 주석은 비즈니스 로직에만 한국어로 작성
- 들여쓰기: 2칸

## 개발 워크플로우

1. `index.html`에 HTML 구조 작성
2. Tailwind CSS 클래스로 기본 스타일링
3. `css/style.css`에 추가 커스텀 스타일 작성
4. `js/main.js`에 인터랙션 기능 구현
5. 로컬 서버로 테스트
6. 반응형 동작 확인 (모바일, 태블릿, 데스크탑)
7. 크로스 브라우저 테스트
8. 배포

## 최적화 체크리스트

- [ ] 이미지 최적화 (WebP 형식 사용 권장)
- [ ] 이미지 lazy loading 적용
- [ ] SEO 메타 태그 추가
- [ ] Open Graph 태그 추가
- [ ] 접근성 검사 (ARIA, 키보드 네비게이션)
- [ ] 성능 측정 (Lighthouse)

## 외부 리소스

### CDN

- **Tailwind CSS**: `<script src="https://cdn.tailwindcss.com"></script>`
- **Font Awesome**: 아이콘 사용
- **Google Fonts**: Inter, Poppins, Noto Sans KR

### 애니메이션 라이브러리 (선택사항)

- AOS (Animate On Scroll)
- GSAP
- Lottie

## 참고 문서

프로젝트의 전체 로드맵과 세부 개발 계획은 `ROADMAP.md`를 참조하세요.
