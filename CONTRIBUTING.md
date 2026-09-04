# Contributing

Thanks for your interest in improving this project! This document explains how
to set up a development environment and get your changes merged.

## Development setup

```bash
git clone https://github.com/opao-max/firecracker-sdk-rs.git
cd firecracker-sdk-rs
cargo --version   # requires a recent stable Rust toolchain
cargo build
```

## Workflow

1. Fork the repository and create a branch from `main`:
   `git checkout -b feat/short-description`
2. Make your change, keeping commits focused and using
   [Conventional Commits](https://www.conventionalcommits.org/):
   `feat:`, `fix:`, `docs:`, `test:`, `refactor:`, `chore:`.
3. Before pushing, run the same checks as CI:

```bash
cargo fmt --all -- --check
cargo clippy --all-targets --all-features -- -D warnings
cargo test --all-features
```

4. Push your branch and open a Pull Request, filling in the PR template.

## Code style

- Format with `rustfmt`; keep clippy warning-free.
- Public items need doc comments with examples where useful.
- Prefer safe Rust; justify any `unsafe` block and add tests around it.
- Semantic-version public API changes; note them in `CHANGELOG.md`.

## Reporting bugs

Please use the Bug Report issue template and include a minimal reproduction.

## License

By contributing, you agree that your contributions will be licensed under the
Apache License 2.0.

