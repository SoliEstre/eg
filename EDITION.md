# EG OS — edition 2026.10.5

> This repository is **composed**, not authored. Every file here is extracted from a single
> upstream commit by `compose-eg.cjs`. Do not edit it in place — fix it upstream and recompose.

| | |
|---|---|
| Edition | `2026.10.5` |
| Upstream | [EstreGenesis](https://github.com/SoliEstre/EstreGenesis) |
| Source commit | `1ed60610a593e7ca73cc5826537bad858c574b60` |
| Source tag | `v2.6.159` |

## Modules in this edition

| Module | Version | Spec |
|---|---|---|
| `estregenesis` | 0.4.2 | _(kit — no spec)_ |
| `constellation` | 0.3.46 | [Constellation.md](Constellation.md) |
| `superscalar` | 0.5.11 | [Superscalar.md](Superscalar.md) |
| `hyperbrief` | 0.9.2 | [Hyperbrief.md](Hyperbrief.md) |
| `greatpractice` | 0.3.5 | [Greatpractice.md](Greatpractice.md) |
| `ultrasafe` | 0.2.16 | [Ultrasafe.md](Ultrasafe.md) |
| `compendium` | 0.2.12 | [Compendium.md](Compendium.md) |
| `corporate` | 0.1.9 | [Corporate.md](Corporate.md) |

**Specification-stage modules** — shipped as a spec, with no plugin to install yet. They are
in this edition because a module spec is the record of what changed, and they are listed
separately because the table above counts what an adopter can *install*.

| Module | Version | Spec |
|---|---|---|
| `Pantty` | v0.4.2 | [Pantty.md](Pantty.md) |

## Seed markers

| File | Marker |
|---|---|
| `AI_Native_Project_Master_Seed_Prompt.md` | v2.7.0 |
| `AI_Native_Project_Seed_Prompt_Compact.md` | v2.7.0 |
| `AI_Native_Project_Seed_Prompt_Lite.md` | v2.7.0 |
| `AI_Native_프로젝트_마스터_시드_프롬프트.md` | v2.7.0 |
| `AI_Native_프로젝트_시드_프롬프트_Compact.md` | v2.7.0 |
| `AI_Native_프로젝트_시드_프롬프트_Lite.md` | v2.7.0 |

## What is not here

- `CHANGELOG-archive.md` — 같은 이유 + 과거 구간
- `CHANGELOG.md` — 상류의 컷 단위 이력이에요. 하루 6~19컷을 그대로 실으면 배포판이 숨기려던 소음을 도로 들여와요 — 대신 EDITION.md 가 이 판의 모듈 버전표 + 상류 링크를 실어요
- `README.md` — 대체됨 — 배포판 README 는 5분 경로 중심으로 따로 저술해요(promo/eg-readme.*)
- `SuperscalarBench.md` — 측정 보고서 — 그림이 docs/assets 에 있고 docs 는 배포판에 안 실려 링크가 깨져요. 모듈 스펙의 근거 자료지 설치물이 아니에요(상류 링크로 충분)
- `_proposals` — 도그푸드 원장 — 개발 기록이지 배포물이 아니에요
- `docs` — 홈페이지는 하나로 둬요 — 두 벌로 만들면 두 벌이 따로 낡아요(판 선택은 배너로)
- `scripts` — 상류 저술 도구(어댑터 생성·참조 회귀 검사) — 배포판에서 돌 일이 없어요

