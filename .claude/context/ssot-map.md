---
asset_class: reference
description: myportfolio SSOT 위치 맵(S7) · 무엇이 정본이고 어떻게 갱신하나
owner: grandmaster
status: active
effective_date: 2026-08-11
lifecycle: 정본 추가·이동·승격 커밋마다 함께 갱신
scope: project(myportfolio)
size_limit: 4KB
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

## 2. 외부 정본 참조

(없음 — 리포 밖 정본 인용은 이 절에만 버전·SHA 병기로 고정한다)
