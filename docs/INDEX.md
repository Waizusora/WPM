# WPM Documentation Index

This directory documents the Wicofe package manager, package formats, repository metadata, and package transactions.

## Whole-system product direction
- [Wicofe system delivery and installation direction 0.1](https://github.com/Waizusora/Wicofe-Docs/blob/main/SYSTEM_DELIVERY_AND_INSTALLATION_DIRECTION_0.1.md) — planned `wpm sync` / `wpm upgrade` user workflow and WPM/Wicofe-Update ownership boundary; command semantics are not finalized.

## Scope
- Package manifest/archive format and versioning.
- Repository metadata, package discovery, and signatures.
- Dependency resolution and version constraints.
- Install, upgrade, removal, ownership database, and rollback.
- Package verification, security policy, and package-manager CLI/API.

## Ownership
WPM owns individual package operations. [Wicofe-Update](https://github.com/Waizusora/Wicofe-Update) owns whole-system update orchestration. [Wicofe-Build](https://github.com/Waizusora/Wicofe-Build) and [Wicofe-Image](https://github.com/Waizusora/Wicofe-Image) produce build and release artifacts.

## Security
Package archives and metadata are untrusted. Specify path traversal protection, archive limits, hashes, signature trust roots, downgrade/replay protection, and transactional rollback before system-wide use.

- [Central Wicofe documentation index](https://github.com/Waizusora/Wicofe-Docs/blob/main/INDEX.md)
- [Repository documentation map](https://github.com/Waizusora/Wicofe-Docs/blob/main/REPOSITORY_DOCUMENTATION_MAP.md)
