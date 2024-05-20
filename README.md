# rust-pre-commit-hooks

My useful pre-commit hooks for Rust.

## Hooks

### `cargo-readme`

Update README.md files with package level docstrings. See [cargo-readme].

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pre-commit-hooks
    rev: vX.Y.Z
    hooks:
      - id: cargo-readme
```

If your package resides in a subdirectory:

```yaml
repos:
  - repo: https://github.com/mondeja/rust-pre-commit-hooks
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

[cargo-readme]: https://github.com/webern/cargo-readme
