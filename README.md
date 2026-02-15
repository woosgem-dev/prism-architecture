# Prism Architecture

> A prism separates white light into a clean spectrum.
> This architecture separates a monolith into **domain bands** with **layered internals**.

**Prism Architecture**는 단일 배포 가능한 풀스택 앱 내부를 `front / back / shared` 3개 도메인으로 분리하고, 프론트엔드 피처를 `ui → logic → service` 3레이어 패키지로 구성하는 아키텍처입니다.

## Live Diagram

**[View Interactive Diagram](https://woosgem-dev.github.io/prism-architecture/)**

## Core Principles

| # | Principle | Description |
|---|----------|-------------|
| 1 | **Domain Triad** | `front/`, `back/`, `shared/` — no direct cross-domain imports |
| 2 | **Shared Bridge** | All cross-domain types live in `shared/types/` only |
| 3 | **Feature Package** | Each feature has its own `package.json` + barrel `index.ts` |
| 4 | **Layer Direction** | `ui → logic → service` (top-down only, no reverse) |
| 5 | **Thin Routing Shell** | `app/` handles routing + layout only. Zero business logic |

## Documentation

- [Full Architecture Reference (Markdown)](./prism-architecture.md)
- [Interactive Diagram (HTML)](./index.html)
