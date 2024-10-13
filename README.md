# mondeja/rust-pc-hooks

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

### `cargo-machete`

Check unused dependencies. See [cargo-machete].

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pc-hooks
    rev: vX.Y.Z
    hooks:
      - id: cargo-machete
```

### `lychee`

Run nightly 'lychee' standalone for fast, async, stream-based link checking.

The [`lychee` repository] includes two hooks for pre-commit, but they need to
have installed `lychee` or `docker` in order to work standalone. This hook
uses pre-commit's Rust machinery to run `lychee` standalone.

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pc-hooks
    rev: vX.Y.Z
    hooks:
      - id: lychee
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
[cargo-machete]: https://github.com/bnjbvr/cargo-machete
[`lychee` repository]: https://github.com/lycheeverse/lychee
