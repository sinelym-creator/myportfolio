---
asset_class: reference
description: PAO(myportfolio) SSOT 위치 맵(S7) · 무엇이 정본이고 어떻게 갱신하나 · S6=해당 없음(단일 파일 제품)
owner: grandmaster
status: active
effective_date: 2026-08-11
lifecycle: 정본 추가·이동·승격 커밋마다 함께 갱신
scope: project(myportfolio)
size_limit: 6KB
---

# SSOT 맵 — myportfolio (S7)

> 세션 시작 시 로드. 정본 추가·이동·승격 커밋에서 함께 갱신한다 — 맵 누락 = 다음 세션에게 그 파일은 없는 것과 같다.

## 1. 정본 명부

| 층 | 정본 | 성격 |
|---|---|---|
| 규범(주법) | `CLAUDE.md` | 프로젝트 고유 규칙 |
| 진행보드 | `PROGRESS.md` | S2 · 현재만(완료 10행 회전) |
| 재개점 | `.claude/context/checkpoint.md` | 세션 스위치 전용 · 3KB |
| 이력 | `CHANGELOG.md` | append 전용 · S2 회전 행선지 |
| 자산 목차 | `project-map.md` | 생성물(수기 편집 금지) |
| 본 맵 | `.claude/context/ssot-map.md` | S7 정본 명부 |
| ▸로드 선언 | `.claude/context/boot-manifest.json` | 역할별 로드 세트 선언 · G2·G5 분모의 원천 · 오케 단독 |
| ▸플랜 | `project-plan.md` | 방향 요약 + 작업 계획 · 오케 기본 로드 · 소형 리포 최소 규격 |

- **S1 `project-overview.md`(에이전트용) = 해당 없음** — 로드 선언에 미선언(018 v0.6 S1 「선언에 `full`로 올린 리포만 의무」) · 사람용 소개는 `README.md`
- **S4(운영절차) = 해당 없음** — 프로젝트 고유 절차 미보유(세션 개폐=연방 절차·배포=Vercel 자동, 규칙은 주법 §2) · 생기면 `docs/operations/` 첫 파일과 함께 등재
- **S6(src맵) = 해당 없음** — 단일 파일 제품(`index.html`)·018 §2 S6 규정의 명시 표기(빈 칸을 만들지 않는다)

## 2. 외부 정본 참조

> 리포 밖 정본 인용은 이 절에만 버전·SHA 병기로 고정한다(본문 산발 인용 금지).

- `claude-infra docs/design/018-project-ssot-standard.md` **v0.8** — 본 리포 칸 구조(7+1 + ▸로드 선언·▸플랜)의 규격 · 참조 세대 = infra **develop `efada7f`**(그 SHA에서 `version: 0.8` 직독 · D-022 재가분)
- `claude-infra docs/design/019-project-migration-plan.md` **v0.7** — 018 적용 절차(T0~T7 · T5에 로드 선언·플랜 신설 편입) · 참조 세대 = infra **develop `efada7f`**(동상 · description v0.7 직독)
- `claude-infra docs/decisions/020-standard-amendment-load-declaration-and-plan.md` — 본 리포 두 파일 신설의 근거(소형 리포 최소 규격) · 참조 세대 = infra **develop `efada7f`**
- `AH(automation-hub) docs/architecture/master-ecosystem-overview.md` v1.1 §3.5 — PAO 정의 · 참조 세대 = AH main `8693b73`(2026-08-11 census) · ⚠ **AH = 구 정본 리포(ADR-010)** — 승계 완료 시 참조처 재지정 대상
