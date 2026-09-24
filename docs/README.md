# DecaVenti Documentation

This directory is the entrypoint for **public, repository-specific** DecaVenti documentation.

## Current Authority

| Subject | Repository authority |
| --- | --- |
| Repository and contributor/agent rules | [`AGENTS.md`](../AGENTS.md) |
| Public project overview | [`README.md`](../README.md) |
| License | [`LICENSE`](../LICENSE) |
| Documentation map | this file |

Additional documentation directories are created only when real content exists. Empty speculative documentation trees
are avoided.

## Public Documentation Boundary

Documentation may explain:
- public client architecture;
- platform behavior;
- public API contracts;
- public security/privacy behavior;
- testing, contribution and release information that is safe to disclose.

Documentation must not disclose:
- private backend source or implementation;
- proprietary algorithms or parameters;
- private datasets or validation internals;
- internal project/repository identifiers, private paths or internal control-plane locators;
- secrets, credentials or private operational evidence.

## Development Model

DecaVenti uses Kotlin Multiplatform and Compose Multiplatform as the primary client stack. The remote service boundary
must remain versioned and implementation-agnostic.

## Governance Projection

A generated `.pheptech/standards-lock.json` is intentionally absent until a qualified **public-safe** projection exists.
It must never be hand-written and must not publish internal governance URLs or IDs.
