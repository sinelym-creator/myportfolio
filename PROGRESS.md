# PROGRESS.md — PAO (myportfolio) 작업 현황판

> 본 파일은 PAO 프로젝트의 Task 현황 단일 SSOT입니다.

## 프로젝트 정체성

**PAO (Project AgentFolio) = AGENT AI 포트폴리오 플랫폼**

- 본질: 개인이 본인의 AI Agent 작업·기억·산출물을 외부에 시각적으로 노출하는 플랫폼
- 현재 단계 (v0.5): **개인 포트폴리오는 PAO 플랫폼의 dogfooding 첫 사례**
- 향후 진화: 다른 사용자도 사용 가능한 플랫폼으로 확장 (사용자 #9416 명시)
- 본질 정합: master-ecosystem v1.0 §3.5 PAO 정의 (`agentFolioLab.liveStats` 라이브 통계)

## 진행 중 (In Progress)

| ID | 설명 | 담당 | 시작일 | 비고 |
|----|------|------|--------|------|

(현재 없음)

## 최근 완료

| ID | 설명 | 완료일 | 산출물 |
|----|------|--------|--------|
| **T-pao-static-v0.5-deploy** | **정적 HTML v0.5 첫 배포** — 사용자 공유 portfolio-final-v0.5.html (1945줄, 다크 + yellow-green accent + 터미널 chrome) GitHub `myportfolio` + Vercel 자동 배포 ✅ | **2026-05-18** | **PR #1 (`068f6f4`), https://younguk-lim-portfolio.vercel.app, AH REGISTRY 6번째 등재** |

## 대기 (Ready) — 우선순위 순

### Phase 1 — Next.js 14 풀 변환 (사이드 cycle)

| ID | 설명 | 우선순위 | 의존 |
|----|------|----------|------|
| T-pao-p1-nextjs-setup | Next.js 14 App Router + TypeScript + Tailwind 셋업 (create-next-app 또는 수동) | P0 | — |
| T-pao-p1-content-json | content JSON 분리 (`src/data/portfolio.json`) — 현 HTML 콘텐츠를 JSON으로 추출 | P0 | T-pao-p1-nextjs-setup |
| T-pao-p1-component | 섹션별 컴포넌트 분리 (Hero·Stack·Experience·Projects·Contact·Footer) | P0 | T-pao-p1-content-json |
| T-pao-p1-fonts-images | next/font (JetBrains Mono·Newsreader·Noto Sans KR) + next/image 최적화 | P1 | T-pao-p1-component |
| T-pao-p1-static-export | next.config.js static export (SSG) — 현 정적 사이트 성능 유지 | P1 | T-pao-p1-fonts-images |

### Phase 0+ — 표준 구조 풀 적용 (AH 템플릿 v3.4)

| ID | 설명 | 우선순위 | 의존 |
|----|------|----------|------|
| T-pao-template-v3.4 | AH 템플릿 v3.4 풀 적용 — CLAUDE.md + INDEX.md + .claude/context/checkpoint.md + .workspace/{feedback,retrospective,tasks,drafts,handoffs,scratch} 신설. **AH Track B4 (setup-new-project.ps1) dogfooding 첫 사례 후보** | P1 | AH Track B4 완료 또는 수동 |

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
| T-pao-multi-tenant | 다중 사용자 plataforma 진화 (현재는 임영욱 1인) — 인증·DB·테넌트 분리 등 | TBD | Phase 2·3 완료 후 사용자 결정 |

## 블로커 (Blocked)

(현재 없음)

## 미해결 / 별 cycle

- Phase 1 Next.js 변환 시점 (사용자 결정)
- 커스텀 도메인 (사용자 보유 도메인 X, 현재 무료 .vercel.app)
- 풀 템플릿 v3.4 적용 (Track B4 dogfooding 첫 사례 또는 수동)

## 관련 (cross-ref)

- AH `~/.claude/registry/snapshots/myportfolio.md` (프로젝트 스냅샷)
- AH `master-ecosystem-overview.md v1.1` §3.5 (PAO 정의)
- 메모리 [[next-session-priorities-2026-05-18]] (③ 신규 프로젝트 추가)
- 메모리 [[user_evolving_system_goal]] (Living System 본질)
- 메모리 [[user_final_goal_apmn]] (APMN 비전)
