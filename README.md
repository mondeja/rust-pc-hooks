# rust-pc-hooks

My useful [pre-commit] hooks for Rust.

## Hooks

### `cargo-readme`

Update README.md files with package level docstrings. See [cargo-readme].

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pc-hooks
    rev: vX.Y.Z
    hooks:
      - id: cargo-readme
```

If your package resides in a subdirectory:

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pc-hooks
    rev: vX.Y.Z
    hooks:
      - id: cargo-readme
        args:
          [
            --project-root=my-subdirectory,
            --output=../README.md,
            --template=../README.tpl,
          ]
```

### `cargo-build-all-features`

Build crate with all feature flag combinations. See [cargo-all-features].

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pc-hooks
    rev: vX.Y.Z
    hooks:
      - id: cargo-build-all-features
```

### `cargo-check-all-features`

Check crate with all feature flag combinations. See [cargo-all-features].

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pc-hooks
    rev: vX.Y.Z
    hooks:
      - id: cargo-check-all-features
```

### `cargo-test-all-features`

Test crate with all feature flag combinations. See [cargo-all-features].

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pc-hooks
    rev: vX.Y.Z
    hooks:
      - id: cargo-test-all-features
```

### `leptosfmt`

Format [Leptos' `view!` macros]. See [leptosfmt].

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pc-hooks
    rev: vX.Y.Z
    hooks:
      - id: cargo-test-all-features
```

[pre-commit]: https://pre-commit.com
[cargo-readme]: https://github.com/webern/cargo-readme
[cargo-all-features]: https://github.com/frewsxcv/cargo-all-features
[leptosfmt]: https://github.com/bram209/leptosfmt
[Leptos' `view!` macros]: https://docs.rs/leptos/latest/leptos/macro.view.html
