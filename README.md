---
asset_class: doc
description: PAO(myportfolio) 개요 · 포트폴리오 정적 사이트와 배포(Vercel) 안내 · S6=해당 없음(단일 파일 제품 index.html)
owner: grandmaster
status: active
effective_date: 2026-08-11
lifecycle: 프로젝트 종료 시 archive
scope: project(pao)
---

# myportfolio

> 임영욱 (LIM YOUNGUK) — Integrated Intelligence Agent AI Builder
> 15+ years senior engineer (C++ 8y + C# 7y → Agent AI environment)

**🌐 배포 URL**: https://younguk-lim-portfolio.vercel.app

## 소개

본 레포는 개인 포트폴리오 정적 사이트(`index.html`)입니다. Vercel을 통해 배포됩니다.

## 기술 스택

- **현재 (v0.5)**: 순수 HTML + CSS (JS 없음, 단일 파일)
  - JetBrains Mono + Newsreader + Noto Sans KR (Google Fonts)
  - Dark theme + Yellow-green accent (#d4ff5e)
  - 터미널 chrome 스타일
- **후속 진화 계획 (Phase 1+)**: Next.js 14 App Router
  - content JSON 분리 + 컴포넌트화
  - Server Components base 라이브 통계 (`agentFolioLab.liveStats`)
  - APMN forward-compat (개인 메모리 노드 연동)

## 배포

- 호스팅: [Vercel](https://vercel.com)
- 자동 배포: `main` 브랜치 push 시 자동 빌드

## 로컬 확인

```bash
# 브라우저에서 index.html 직접 열기
start index.html

# 또는 간단한 로컬 서버
python -m http.server 8000
# → http://localhost:8000
```

## 라이센스

본 레포의 코드는 개인 포트폴리오 용도이며, 콘텐츠(이력·경력 등)는 임영욱 본인의 소유입니다.
