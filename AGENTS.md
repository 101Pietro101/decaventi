# DecaVenti — Repository Operating Contract

> This file is repository-owned and versioned. Internal PhepTech governance remains authoritative for actor authority,
> lifecycle and transaction control; this public repository intentionally does not mirror internal control-plane
> records, identifiers or private architecture details.

## Scope

DecaVenti is a **public R&D application** built around Kotlin Multiplatform and Compose Multiplatform.

This repository owns public client concerns only:
- cross-platform UI and UX;
- client-side application logic;
- local persistence and networking;
- authentication client integration;
- versioned public request/response contracts;
- public tests, examples and documentation that are safe to disclose.

A remote service may fulfill backend operations. Its private implementation is outside this repository.

## Public Disclosure Firewall

Never commit, generate, mirror, embed or document:
- private backend source or private Git history;
- implementation-equivalent backend binaries or payloads;
- proprietary algorithms, formulas, weights, thresholds or internal method identifiers;
- private datasets, validation corpora or internal diagnostics;
- internal repository/project names, private paths, private hashes or internal control-plane URLs/IDs;
- credentials, tokens, private keys, signing identities or production trust material.

Public contracts must describe **what** the client sends/receives, not **how** the remote implementation computes results.

When disclosure safety is uncertain, STOP and require explicit review before commit.

## Operating Model

Internal PhepTech PMM-HAI governance applies. INCOSE / INCOSE-based Systems Engineering is not adopted for this project.

Actor boundaries:
- **Pietro** — final decision authority, risk owner, protected `main` and direct production authority.
- **ChatGPT** — Co-Project Manager; architecture, review, governance and W4 documentation writer with Pietro.
- **Codex** — bounded Engineering Delivery Actor after objective admission.

Absolute rules:
- Codex must never create, edit or repair W4 documentation, including this `AGENTS.md`.
- Codex must never commit, push, merge, reset, rebase, rename, delete or otherwise mutate `main`.
- Codex works only on explicitly authorized `work/codex/*` branches.
- Technical evidence or green tests never imply release, production, Store or lifecycle approval.

## Git Operating Model

Operational remote: public GitHub repository `101Pietro101/decaventi`.

- `main` is the protected permanent integration surface for Pietro/ChatGPT only.
- Routine work uses `work/<actor>/<task>`.
- Pietro uses `work/pietro/<task>`.
- ChatGPT uses `work/chatgpt/<task>`.
- Codex uses `work/codex/<task>` only after admission.
- Integrate permanent branches through reviewed pull requests.
- Auto-merge, force-push and history rewrite are prohibited unless explicitly authorized for the exact operation.
- Preserve unrelated changes and the existing MPL-2.0 license.
- Remote mutation requires a fresh workflow/provider-trigger preflight; ambiguity is fail-closed.
- Release, Store, signing, deployment and provider actions require separate authority.

## Licensing

Repository source governed by the Mozilla Public License 2.0 must remain compliant with the tracked `LICENSE`.

Do not add incompatible third-party code or assets without a license review. Dependency metadata and notices must remain
accurate when dependencies are introduced.

## Technical Direction

- Prefer Kotlin Multiplatform and Compose Multiplatform for shared client code and UI.
- Keep platform-specific code behind explicit platform boundaries.
- Keep the public API client implementation-agnostic.
- Do not embed private backend logic in JVM/native/WASM/client artifacts.
- Prefer typed contracts, structured concurrency, explicit errors and deterministic client behavior.
- Add technologies only when a concrete client-side need justifies them.

## Documentation

Public repository documentation belongs in `docs/**`, root `README.md` and this `AGENTS.md`.

Only public-safe information belongs here. Internal lifecycle records, private design rationale and confidential evidence
remain in the internal control plane and must not be copied into public files.

W4 is Pietro/ChatGPT-only. Codex may read public documentation and report findings but may not create, edit or repair it.

## Generated And Transient State

Repository-owned generated/transient outputs belong under project-controlled generated roots, normally `build/` and
`build/temp/`, and must be Git-excluded and disposable.

Exceptional retained evidence is not a public dumping ground. Do not commit logs, caches, backup archives, credentials
or private evidence.

## Generated Governance Projection

`.pheptech/standards-lock.json` is generated/deterministic and must not be manually created or edited.

A future public projection must be explicitly qualified as **public-safe** and must not expose internal URLs, IDs or
private authority metadata. Until that qualified projection exists, its absence is intentional.

## Quality And Stop Conditions

STOP before mutation when:
- the current task or write set is ambiguous;
- an intended path/ref is outside the explicit mandate;
- another writer overlaps the same surface;
- a change risks disclosing private implementation or internal metadata;
- a secret/license/security finding is unresolved;
- a provider mutation could trigger unauthorized cost or execution;
- the task would require Codex to write W4 or mutate `main`.

No public commit is worth weakening the private/public boundary.
