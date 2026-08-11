---
asset_class: directive
description: myportfolio 주법 · 이 프로젝트에서만 참인 규칙(연방 헌법 위)
owner: grandmaster
status: active
effective_date: 2026-08-11
lifecycle: 연방 헌법 개정 시 review · 프로젝트 종료 시 archive
scope: project(myportfolio)
size_limit: 50lines
---

# myportfolio — 주법 (프로젝트 지침)

> **연방 헌법(글로벌 지침)이 기본이다.** 이 문서에는 **이 프로젝트에서만 참인 것**만 적는다.
> 🔴 연방에 이미 있는 것(커밋 규약·보안 규칙·보고 형식)을 여기 다시 쓰지 않는다 — 두 곳에 적히는 순간 둘이 갈라진다.

## 1. 무엇인가

PAO(Project AgentFolio) - 개인 AI Agent 작업·산출물을 노출하는 포트폴리오 플랫폼(현 v0.5 = 정적 단일 파일 dogfooding)

## 2. 도메인 제약

> 이 프로젝트에서만 참인 사실 — 대상 사용자·규제·외부 연동·기술 제약.

- ⚠ 작성 필요

## 3. 프로젝트 고유 규칙

> 연방과 **다르게** 가야 하는 것 + 그 사유. 다른 게 없으면 「없음」이라고 적는다(빈칸으로 두지 않는다).

- 없음

## 4. 지금

| 알고 싶은 것 | 어디 |
|---|---|
| 지금 뭐 하는 중인가 | `.claude/context/checkpoint.md` — **재개는 이 파일 1 Read로 끝난다** |
| 현황·결정 이력 | `PROGRESS.md` |
| 이 리포에 뭐가 있나 | `project-map.md` — 🔴 생성물이다. 수기 편집 금지 |

## 5. 자산을 만들 때

```
pwsh C:/Users/sinel/repos/claude-infra/tools/scaffold.ps1 -Class <class> -Name <name> -RepoRoot .
```
- **경로를 외우지 않는다** — `asset_class`를 고르면 배치는 등록부가 정한다(설계 006 R-1).
- **빈 폴더를 미리 만들지 않는다** — 디렉터리는 첫 자산이 태어날 때 생긴다(R-2).
- 새 자산 종류가 필요하면 폴더가 아니라 **등록부에 1줄**을 추가한다(R-3).
