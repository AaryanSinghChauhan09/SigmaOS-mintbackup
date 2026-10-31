# SigmaOS MintBackup

This `no_std` crate contains a small backup API model inspired by Linux Mint's
MintBackup. It does not read files, create archives, store backup records, or
restore user data. `create_backup` only increments an in-memory counter and
returns success; `restore_backup` returns success without checking the ID or
restoring anything.

The existing unit checks cover these model-level return values only. They do
not verify backup or recovery behavior.

## Build

```sh
cargo check --lib
```

## License

Apache-2.0. See [`Cargo.toml`](Cargo.toml).

## Inspiration

This component is inspired by Linux Mint and Omarchy Linux to provide:
- Single responsibility: One clear purpose
- Loose coupling: Minimal dependencies
- Stable interfaces: Well-defined APIs

## Status

- Architecture: Designed
- Implementation: Planned
- Testing: Planned
