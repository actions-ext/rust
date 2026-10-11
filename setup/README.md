# setup

Configure a Rust toolchain, optional targets and components, and caching.

## Usage

```yaml
- name: Setup Rust
  uses: actions-ext/rust/setup@3b918cc2cb4a231ad3752f8cc129da5f07626ce2
  with:
    targets: wasm32-unknown-unknown
```

Only the host target is installed by default. Use `targets` for additional architectures or WASM. Install Cargo tools in your project's development setup.

## Inputs

| Name         | Default          | Description                        |
| :----------- | :--------------- | :--------------------------------- |
| `toolchain`  | `stable`         | Rust toolchain to install.         |
| `components` | `clippy,rustfmt` | Comma-separated rustup components. |
| `targets`    | Empty            | Comma-separated Rust targets.      |
