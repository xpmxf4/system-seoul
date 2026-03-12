# SYSTEM SEOUL Website - Project Notes

이 파일은 SYSTEM SEOUL 웹사이트 프로젝트의 작업 내역과 설정을 기록합니다.

---

## 🎨 디자인 가이드라인

### 폰트
- **글로벌 폰트**: Acumin Pro (Adobe Fonts)
- **Adobe Fonts CSS**: `https://use.typekit.net/zwy6jmq.css`
- **font-family**: `"acumin-pro", sans-serif`
- **가중치**: Regular (400), Bold (700)

### 색상
- **배경**: 검정 (`#000000`)
- **주요 색상 (Primary)**: 주황 (`#ec5b13`)
- **GNB 링크 활성**: `#FFF` (white)
- **GNB 링크 비활성**: `white/50` (50% opacity) hover 시 white

### GNB (Global Navigation Bar)
- **구조**: 모든 페이지 동일
- **클래스**: `sticky top-0 z-50 w-full border-b-0 sticky-nav`
- **높이**: `h-16`
- **링크 간격**: `gap-10`
- **폰트**: `text-xs font-bold uppercase tracking-widest`
- **활성 상태**: `text-white`
- **비활성 상태**: `text-white/50 hover:text-white transition-colors`
- **좌우측 아이콘**: 없음 (제거됨)
- **Border**: 없음 (`border-b-0`)

### 페이지별 GNB 활성 링크
- **HOME**: Home 링크 활성
- **VIDEO**: Video 링크 활성
- **TOUR**: Tour 링크 활성

### 스크롤바
- **VIDEO, TOUR 페이지**: 스크롤바 숨김 (`::-webkit-scrollbar { width: 0px; background: transparent; }`)

### Footer
- **저작권 텍스트**: `© 2026 mineral. All Rights Reserved.`

---

## 📄 페이지 구조

### HOME (home-logo-refined.html)
- **로고 크기**: `w-[22.4rem] h-[22.4rem] md:w-[33.6rem] md:h-[33.6rem]` (1.4배 확대)
- **메인 콘텐츠 위치**: `-mt-52`
- **플랫폼 아이콘 위치**: `bottom-[10rem]`
- **GNB 패딩**: `pt-16`

### VIDEO (video-dark-minimal.html)
- **GNB 패딩**: `pt-16`

### TOUR (tour-dark-minimal.html)
- **GNB 패딩**: `pt-16`

---

## 🔧 배포 정보

- **브랜치**: `gh-pages`
- **배포 URL**: `https://xpmxf4.github.io/system-seoul/`
- **원격 저장소**: `https://github.com/xpmxf4/system-seoul.git`

---

## 📝 작업 내역

### 2026-03-12
1. **GNB 링크 수정**: 모든 페이지 간 링크 연결 확인
2. **GNB 스타일 통일**: TOUR 페이지 스타일을 모든 페이지에 적용
3. **GNB 아이콘 제거**: TOUR 좌측 person 버튼, VIDEO 우측 아이콘 제거
4. **폰트 변경**: Public Sans → Plus Jakarta Sans → Acumin Pro
5. **GNB border 색상**: `border-neutral-muted/30` → `border-black/80` → 제거 (`border-b-0`)
6. **스크롤바 제거**: VIDEO, TOUR 페이지
7. **HOME 로고 조정**: 1.4배 확대, 위치 위로 이동 (-mt-52), 플랫폼 아이콘 bottom-[10rem]
8. **GNB 비활성 링크 밝기 조정**: `rgb(68 68 68 / 0.4)` → `white/60`
9. **Footer 텍스트 변경**: © 2026 미네랄 → © 2026 mineral
10. **GNB 비활성 링크 조정**: white/60 → white/50
11. **Footer 텍스트 추가**: 모든 페이지에 "All Rights Reserved." 추가

---

## 🔄 향후 작업시 참고사항

1. **모든 페이지 변경 시 GNB 통일 유지**: 3개 페이지 모두 동일한 GNB 구조 유지
2. **폰트 변경 시 Tailwind config와 CSS 동시 수정**: `font-display` 클래스와 inline style 모두 확인
3. **Adobe Fonts**: Acumin Pro는 유료 폰트, Web Project ID: `zwy6jmq`
4. **커밋 메시지**: 한글로 작성, 변경사항 명확히 기술
5. **배포 후 강력 새로고침**: 브라우저 캐시 문제로 Ctrl+Shift+R (Cmd+Shift+R) 안내

---

## 🚀 빠른 배포 명령어

```bash
# 변경사항 커밋 및 푸시
git add -A
git commit -m "메시지"
git push origin gh-pages
```
