# DecaVenti

DecaVenti is a public R&D application built with **Kotlin Multiplatform** and **Compose Multiplatform**.

The project is designed as a cross-platform client for Android, iOS, Desktop and Web. Client functionality that depends
on remote computation uses a versioned service contract; the service implementation is intentionally outside this
repository.

## Repository Scope

This repository may contain:
- KMP/CMP application code;
- public UI and UX;
- client persistence and networking;
- authentication client integration;
- public API contracts;
- public tests, examples and documentation.

It does **not** contain private backend implementation or proprietary server-side logic.

## Status

Repository governance foundation is being established before application implementation begins.

## Start Here

1. Read [AGENTS.md](AGENTS.md).
2. Read [docs/README.md](docs/README.md).
3. Use a scoped `work/<actor>/<task>` branch for changes.
4. Keep all public contributions within the disclosure and licensing boundaries.

## License

DecaVenti is licensed under the [Mozilla Public License 2.0](LICENSE).
