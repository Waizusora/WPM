# WPM — Wicofe Package Manager

WPM is the planned native package manager for installing, updating, querying, and removing Wicofe software.

## Scope

- Package manifest and archive format.
- Repository metadata and package discovery.
- Dependency resolution and version constraints.
- Integrity verification and package authenticity.
- Transactional installation, upgrade, removal, and rollback behavior.
- Package ownership database and filesystem integration.

## Security requirements

Package metadata and archives are untrusted input. Define path traversal protections, archive limits, hash verification, signature trust roots, downgrade policy, and atomic transaction behavior before enabling system-wide installation.

## Boundaries

WPM owns package operations and package metadata. Wicofe-Build and Wicofe-Image produce build and image artifacts; Wicofe-Update owns OS update orchestration. These formats must be explicitly related rather than conflated.

## Status

Initial repository baseline. Package format, repository protocol, and signature policy require formal specification before being considered stable.

## License

Original project code targets MPL-2.0; dependencies require individual license review.
