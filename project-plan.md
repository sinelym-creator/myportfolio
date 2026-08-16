---
asset_class: reference
description: PAO(myportfolio) 플랜 · 방향 요약 + 확정 작업 계획 단일본 · 오케스트레이터 기본 로드 · 소형 리포 최소 규격(018 v0.6 §6)
owner: grandmaster
status: active
effective_date: 2026-08-17
lifecycle: 세션마다 재작성하지 않는다 · summarizes 대상이 바뀔 때만 갱신
scope: project(myportfolio)
size_limit: 3KB
version: 0.1
# 🔴 요약 대상. 이 리포에는 docs/ 자체가 없어 요약할 층이 0이다 — 층이 생기면 이 배열에 1줄 추가.
summarizes: []
---

# PAO 플랜 (myportfolio)

## 0. 방향

PAO(Project AgentFolio)는 개인이 자신의 AI Agent 작업·기억·산출물을 외부에 시각적으로 노출하는
포트폴리오 플랫폼이고, 현 v0.5는 그 dogfooding 첫 사례인 **정적 단일 파일**(`index.html` · 순수
HTML+CSS · Vercel 자동 배포)이다. 제품이 파일 하나이므로 src맵(S6)은 해당 없음이고, `main` 병합은
곧 라이브 배포다. 다음 방향은 Next.js 14 App Router 변환(콘텐츠 JSON 분리·컴포넌트화)과 그 위의
라이브 통계(`agentFolioLab.liveStats`)이며, 착수 시점은 폐하 결정 사항이다.

## 3. 작업 계획 (티켓)

> 원천 = `PROGRESS.md` 「해야 할 일」 · `.claude/context/checkpoint.md` 「다음」. 상세·의존은 그쪽이 정본이고
> 여기는 방향과 붙은 상위 3건만 둔다(플랜은 보드를 복제하지 않는다).

| ID | 티켓 | 우선순위 | 상태 |
|---|---|---|---|
| T-pao-p1-nextjs-setup | Next.js 14 App Router + TypeScript + Tailwind 셋업 | P0 | 대기 — 착수는 폐하 결정 |
| T-pao-p1-content-json | 콘텐츠 JSON 분리(`src/data/portfolio.json`) — 현 HTML 콘텐츠 추출 | P0 | 대기 — setup 의존 |
| T-pao-p2-live-stats | `agentFolioLab.liveStats` 라이브 통계 통합(Server Components) | P2 | 대기 — Phase 1 완료 후 |

> 018 표준 마이그레이션(019 T0~T7)은 이 리포에서 **종료**됐다 — 재게이트를 걸지 않는다
> (재개 시 확인 정본 = claude-infra `PROGRESS.md`).
