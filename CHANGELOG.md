# Changelog — king-arch

Todas las notas relevantes de este plugin. Formato basado en [Keep a Changelog](https://keepachangelog.com/),
versionado [SemVer](https://semver.org/).

## [1.0.0] — 2026-05-29

### Added (A6 — extracción desde king-core)

Plugin nuevo extraído de king-core como parte del decouple A6 (medium-risk), replicando el patrón de A3
(king-content / king-infra). king-arch declara `requires: ["king-framework"]` y lee agentes, knowledge compartido
(`architecture-patterns.md`, `resilience-patterns.md`) y `session-management` de king-core cross-plugin.

- **12 skills de arquitectura** (anatomía v2.0): `clean-arch-setup`, `hexagonal-setup`, `ddd-tactical`, `cqrs-setup`,
  `event-sourcing`, `saga-design`, `resilience-weave`, `idempotency`, `api-contract-first`, `contract-test-pact`,
  `microservice-extract`, `event-broker-setup` (+ sus 12 commands).
- **2 knowledge files** de dominio exclusivos: `knowledge/domain/saga-patterns.md`,
  `knowledge/domain/distributed-systems.md`.
- **`skills/_shared/`** duplicado desde king-core (contratos transversales: lifecycle-outputs, castle-capas,
  skill-envelope, if-fails-templates y dependencias transitivas) para resolución intra-plugin robusta.

Origen: estas 12 skills fueron entregadas en M04 (king-core) y se trasladan aquí sin cambios de comportamiento.
