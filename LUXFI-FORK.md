# LUXFI-FORK

This is a luxfi-maintained fork of [ethereum/c-kzg-4844](https://github.com/ethereum/c-kzg-4844).

## Pin

* Upstream tag: `v2.1.7`
* Commit SHA: `9f4bcc83cbb17b3dbc3432de7320790968143ab9`
* License: Apache-2.0 (see `LICENSE`)

## Why this fork exists

c-kzg-4844 is the canonical KZG commitment library for EIP-4844 / Verkle.
luxcpp/crypto consumes it via FetchContent for the `kzg/` body (LP-137 sibling
#103); lux/crypto Go layer wraps it via `github.com/ethereum/c-kzg-4844/v2`.

Owning the fork lets luxfi pin a specific commit per release branch and avoid
breaking changes between upstream `v2.x` minor bumps.

## Sync policy

* Track upstream `v2.x` releases only.
* Pull upstream tags into `sync/<tag>` branches. Audit the diff. Re-run KZG
  KATs in `luxcpp/crypto/kzg`. Merge to `main` only after KATs pass.
* Trusted setup updates require explicit luxfi-crypto-team review. Never
  auto-sync setup files.

## Maintainer

luxfi crypto team. Contact via the `luxfi/crypto` repo.
