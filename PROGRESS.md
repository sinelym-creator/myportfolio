---
asset_class: ssot
description: PAO(myportfolio) 현황·결정 이력 SSOT · S2 보드(진행중·완료·블로커·해야 할 일)
owner: grandmaster
status: active
effective_date: 2026-08-11
lifecycle: 트랙 종료 시 archive · 성장 게이트 대상(완료 10행 초과분은 CHANGELOG 회전)
scope: project(pao)
---

# PROGRESS.md — PAO (myportfolio) 작업 현황판

> 본 파일은 PAO 프로젝트의 Task 현황 단일 SSOT입니다.

## 프로젝트 정체성

**PAO (Project AgentFolio) = AGENT AI 포트폴리오 플랫폼**

- 본질: 개인이 본인의 AI Agent 작업·기억·산출물을 외부에 시각적으로 노출하는 플랫폼
- 현재 단계 (v0.5): **개인 포트폴리오는 PAO 플랫폼의 dogfooding 첫 사례**
- 향후 진화: 다른 사용자도 사용 가능한 플랫폼으로 확장 (사용자 #9416 명시)
- 본질 정합: master-ecosystem v1.0 §3.5 PAO 정의 (`agentFolioLab.liveStats` 라이브 통계)

## 진행 중

| ID | 설명 | 담당 | 시작일 | 비고 |
|----|------|------|--------|------|
| MIG-PAO-018 | 018 「7+1칸」 표준 마이그레이션 파일럿(019 T0~T7) | 루루슈 | 2026-08-11 | T7 리바이 게이트 대기 |

## 완료

> 상한 10행 · 상세 원문은 `CHANGELOG.md` 회전분에 보존(018 ▸이력).

| ID | 설명 | 완료일 | 산출물 |
|----|------|--------|--------|
| T-pao-mobile-scroll-hotfix | 모바일 스크롤 빈 화면 핫픽스 — reveal threshold 0.1→0 + 3초 force-reveal 안전망 | 2026-06-16 | PR #8 (`b51404f`) |
| T-pao-anim-effects | 시각·동적 효과 + 콘텐츠 수정 — 진행바·reveal·카운트업·타이핑 등 + reduced-motion 정책 | 2026-06-16 | PR #7 (`f6d15d7`) |
| T-pao-v0.6-overhaul-deploy | 전면 개편 + 배포 — featured 7카드 3그룹 재구성·경력 15.7년 완성·민감내용 제외 | 2026-06-15 | PR #6 (`5be5ec9`) |
| T-pao-i18n-toggle | KO/EN 토글 + 영문 풀 번역 — lang attribute 토글·localStorage·87 span pairs | 2026-05-18 | PR #4 (`c8ef5aa`) |
| T-pao-static-v0.5-deploy | 정적 HTML v0.5 첫 배포 — Vercel 자동 배포 | 2026-05-18 | PR #1 (`068f6f4`) |

## 블로커

(현재 없음)

## 해야 할 일 — 우선순위 순

### Phase 1 — Next.js 14 풀 변환 (사이드 cycle)

| ID | 설명 | 우선순위 | 의존 |
|----|------|----------|------|
| T-pao-p1-nextjs-setup | Next.js 14 App Router + TypeScript + Tailwind 셋업 (create-next-app 또는 수동) | P0 | — |
| T-pao-p1-content-json | content JSON 분리 (`src/data/portfolio.json`) — 현 HTML 콘텐츠를 JSON으로 추출 | P0 | T-pao-p1-nextjs-setup |
| T-pao-p1-component | 섹션별 컴포넌트 분리 (Hero·Stack·Experience·Projects·Contact·Footer) | P0 | T-pao-p1-content-json |
| T-pao-p1-fonts-images | next/font (JetBrains Mono·Newsreader·Noto Sans KR) + next/image 최적화 | P1 | T-pao-p1-component |
| T-pao-p1-static-export | next.config.js static export (SSG) — 현 정적 사이트 성능 유지 | P1 | T-pao-p1-fonts-images |

### Phase 2 — 라이브 통계 통합

| ID | 설명 | 우선순위 | 의존 |
|----|------|----------|------|
| T-pao-p2-live-stats | `agentFolioLab.liveStats` Server Components base 외부 데이터 fetch — totalAgentEdits·activeProjects·lastDeploy timestamp 등 | P2 | Phase 1 완료 |

### Phase 3 — APMN forward-compat

| ID | 설명 | 우선순위 | 의존 |
|----|------|----------|------|
| T-pao-p3-apmn | Personal Memory Node Network 연동 — 개인 메모리 노드 ↔ 포트폴리오 자동 갱신 | P3 | APMN 비전 진입 (Phase 4+) |

### 플랫폼화 — 다른 사용자도 사용 가능한 플랫폼 (사용자 #9416 명시)

| ID | 설명 | 우선순위 | 의존 |
|----|------|----------|------|
| T-pao-multi-tenant | 다중 사용자 플랫폼 진화 (현재는 임영욱 1인) — 인증·DB·테넌트 분리 등 | TBD | Phase 2·3 완료 후 사용자 결정 |

## 미해결 / 별 cycle

- Phase 1 Next.js 변환 시점 (사용자 결정)
- 커스텀 도메인 (사용자 보유 도메인 X, 현재 무료 .vercel.app)
- ~~풀 템플릿 v3.4 적용 (Track B4 dogfooding 첫 사례 또는 수동)~~ → 2026-08-11 **018 표준 골격 adopt로 대체 이행**(구 AH 템플릿 축 폐지 — T-pao-template-v3.4 종결)

## 결정 이력

> 현재 유효 결정만의 참조 표(이력 축적 아님) — 상한 5행 · 초과분은 `CHANGELOG.md`로 회전(018 ▸이력 D1).

| 일시(KST) | 결정 | 결정자 |
|---|---|---|
| 2026-08-11 | 018 표준 마이그레이션 파일럿 대상 확정(Q5 ①) · 순서=스캐폴드 완성 선행 | 폐하 (`1536728691990728775`) |

## 관련 (cross-ref)

- AH `~/.claude/registry/snapshots/myportfolio.md` (프로젝트 스냅샷) — ⚠ AH=구 정본 리포(ADR-010)
- AH `master-ecosystem-overview.md v1.1` §3.5 (PAO 정의) — 외부 정본 참조는 `ssot-map.md` §2가 정본
- 메모리 [[next-session-priorities-2026-05-18]] (③ 신규 프로젝트 추가)
- 메모리 [[user_evolving_system_goal]] (Living System 본질)
- 메모리 [[user_final_goal_apmn]] (APMN 비전)
