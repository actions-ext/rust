# setup

Configure a Rust toolchain, optional targets and Cargo tools, and caching.

## Usage

```yaml
- name: Setup Rust
  uses: actions-ext/rust/setup@7d919b14e08dc1155a267dffbcc58260bdfdd63b
  with:
    targets: wasm32-unknown-unknown
    tools: |
      cargo-nextest@0.9.140
      cargo-llvm-cov@0.8.7
```

Cargo tools require `crate@version` entries and are installed with an exact version requirement.

## Inputs

| Name         | Default          | Description                                              |
| :----------- | :--------------- | :------------------------------------------------------- |
| `toolchain`  | `stable`         | Rust toolchain to install.                               |
| `components` | `clippy,rustfmt` | Comma-separated rustup components.                       |
| `targets`    | Empty            | Comma-separated Rust targets.                            |
| `tools`      | Empty            | Newline-separated Cargo tools in `crate@version` format. |
| `cache_key`  | `rust`           | Additional Rust cache key.                               |
