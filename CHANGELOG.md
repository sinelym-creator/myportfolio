---
asset_class: changelog
description: myportfolio 이력 · S2 「완료」 회전분의 행선지(append 전용)
owner: grandmaster
status: active
effective_date: 2026-08-11
lifecycle: 분기별 초과 시 docs/reports/ 절단 이관 review
scope: project(myportfolio)
---

# CHANGELOG — myportfolio

> append 전용 · S2 「완료」 축 회전분은 여기에만 쌓인다(표준 018 ▸이력 칸).

## 2026-08-11

- 표준 골격 적용

## 2026-08-11 — 구 PROGRESS 「최근 완료」 상세 회전분 (원문 무수정 이관 · 019 T3)

| ID | 설명 | 완료일 | 산출물 |
|----|------|--------|--------|
| **T-pao-mobile-scroll-hotfix** | **모바일 스크롤 빈 화면 핫픽스 (폐하 1:1 긴급)** — reveal-on-scroll IntersectionObserver `threshold:0.1`이 모바일 단일컬럼 긴 섹션(뷰포트 10배+)에서 10% 노출 미달로 등장 미발동 → `.revealed` 미부여 → `opacity:0` 고정(첫 스크롤 시 화면 하단 빈 화면). 데스크탑은 짧은 다컬럼이라 정상 → 모바일에서만 발현. 수정: ① threshold 0.1→0(요소가 화면에 닿는 즉시 등장·높이 무관 안전) ② 3초 force-reveal 안전망 setTimeout(미등장 요소 강제표시·영구 비표시 차단). index.html 9줄·데스크탑 동작/기존 연출 영향 0. develop `83daf7b`→PR #8→main 머지→Vercel success→라이브 fetch 검증 ✅(서빙 HTML threshold:0+안전망 반영·옛 0.1 잔존 0)·**폐하 모바일 직접 확인 완료** | **2026-06-16** | **PR #8 (`b51404f`), https://younguk-lim-portfolio.vercel.app** |
| **T-pao-anim-effects** | **시각/동적 효과 + 콘텐츠 수정 (PAO-PORTFOLIO-ANIM)** — 어시스턴트 고유명(제니퍼·Nova) 제거 + 동적효과 신설(스크롤 진행바·섹션 reveal·stat 카운트업·복사 버튼·카드 hover lift·hero 타이핑·3레이어 스택 연결흐름·타임라인 마커 pulse/ripple) + reduced-motion 정책(콘텐츠 진입모션 off·장식 무한모션 항상on=설정무관) + D1 오케스트레이션 다이어그램 신설→폐하 피드백으로 제거(D2 3레이어 스택 유지). 폐하 실시간 프리뷰 피드백 루프 다회 반영: 첫화면 first-paint(hero 제목 타이핑이 ~1.2s 빈채 대기→즉시표시 수정)·AF live-link 데스크탑 한줄(nowrap)·타임라인 서클 절제(glow→scale 방식). develop→PR #7→main 머지→Vercel 배포→라이브 fetch 검증 ✅ (신규효과 전부 반영·D1/고유명 제거 확인) | **2026-06-16** | **PR #7 (`f6d15d7`), https://younguk-lim-portfolio.vercel.app** |
| **T-pao-v0.6-overhaul-deploy** | **포트폴리오 전면 개편 + 프로덕션 배포 (세바스 전담 첫 작업)** — featured_work 7카드 재구성(3그룹 맥락분리·최신순): [AI work] autoflowagent 플래그십·automation-hub·claude-ops 신설 / [현재 회사 업무] 스포츠·곤충 간략화+기밀노트 / [시니어 트랙] 엔터프라이즈 SI + **첫 회사 통신인프라 C++ 7.5년 신설 → 15.7년 완성**. 민감내용 제외(회사도메인·상세스택)·pgvector 정정(미확정→일반표현, CO 유지)·tech_stack 보강(NestJS·Next.js·MCP Discord·AF/CO 에이전트플랫폼)·ADR 전문용어 9곳 제거·AF Tailscale 라이브 링크(개인시연)·access scope AF/CO. develop→PR #6→main 머지→배포→라이브 fetch 7카드 검증 ✅ (폐하 윤허 기반 단계 진행) | **2026-06-15** | **PR #6 (`5be5ec9`), https://younguk-lim-portfolio.vercel.app** |
| **T-pao-i18n-toggle** | **KO/EN 토글 + 영문 풀 번역** — 헤더 KO/EN UI 정적 → 기능화. W3C 표준 `lang` attribute 토글 (html[lang="ko"]/[lang="en"] 셀렉터) + localStorage 영속 + 87 inline 병행 span pairs. index.html 1945 → 2138줄 (+193). 10 섹션 전부 커버 (hero·the_shift·timeline·5 project cards·tech_stack·lab·credentials·external_signals·contact·footer). 라이브 사이트 raw curl + WebFetch 양 언어 정상 노출 검증 ✅ | **2026-05-18** | **PR #4 (`c8ef5aa`), https://younguk-lim-portfolio.vercel.app (i18n live)** |
| **T-pao-static-v0.5-deploy** | **정적 HTML v0.5 첫 배포** — 사용자 공유 portfolio-final-v0.5.html (1945줄, 다크 + yellow-green accent + 터미널 chrome) GitHub `myportfolio` + Vercel 자동 배포 ✅ | **2026-05-18** | **PR #1 (`068f6f4`), https://younguk-lim-portfolio.vercel.app, AH REGISTRY 6번째 등재** |
