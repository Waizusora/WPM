# WPM — Wicofe Package Manager

WPM is the planned native package manager for installing, updating, querying, and removing Wicofe software.

## Scope

- Package manifest and archive format.
- Repository metadata and package discovery.
- Dependency resolution and version constraints.
- Integrity verification and package authenticity.
- Transactional installation, upgrade, removal, and rollback behavior.
- Package ownership database and filesystem integration.

## Planned Terminal command direction

The proposed user-facing examples are `wpm sync` (refresh trusted metadata and discover updates) and `wpm upgrade` (apply eligible updates). These commands are not implemented or finalized. WPM owns package operations; if the commands also expose whole-system updates, they must delegate release staging/activation to Wicofe-Update rather than taking over its responsibility. See the [system delivery and installation direction](https://github.com/Waizusora/Wicofe-Doc/blob/main/SYSTEM_DELIVERY_AND_INSTALLATION_DIRECTION_0.1.md).

## Security requirements

Package metadata and archives are untrusted input. Define path traversal protections, archive limits, hash verification, signature trust roots, downgrade policy, and atomic transaction behavior before enabling system-wide installation.

## Boundaries

WPM owns package operations and package metadata. Wicofe-Build and Wicofe-Image produce build and image artifacts; Wicofe-Update owns OS update orchestration. These formats must be explicitly related rather than conflated.

## Status

Initial repository baseline. Package format, repository protocol, and signature policy require formal specification before being considered stable.

## License

Original project code targets MPL-2.0; dependencies require individual license review.

## Documentation index

See [docs/INDEX.md](docs/INDEX.md) for this repository's technical documentation. The [central repository documentation map](https://github.com/Waizusora/Wicofe-Doc/blob/main/REPOSITORY_DOCUMENTATION_MAP.md) identifies canonical ownership and cross-repository boundaries.

## Wicofe-wide principles

Wicofe is an independent Unix-like, POSIX-compatible operating system and software ecosystem, designed as an alternative to established and widely adopted software ecosystems and technologies, including GNU. Native components must use Wicofe interfaces and must not require Linux libc or GNU compatibility layers. Prefer permissive licenses; avoid GPL/AGPL, and consider LGPL only when no suitable permissive alternative exists. Reuse or fork upstream software when implementing it from scratch would be disproportionately difficult. See the [canonical project principles](https://github.com/Waizusora/Wicofe-Doc/blob/main/PROJECT_PRINCIPLES.md).
