# goldsrc-template-plugin-rust

[![CI](https://github.com/goldsrc-rs/goldsrc-template-plugin-rust/actions/workflows/ci.yml/badge.svg)](https://github.com/goldsrc-rs/goldsrc-template-plugin-rust/actions)
[![License](https://img.shields.io/badge/license-MIT%2FApache--2.0-blue.svg)](LICENSE-MIT)
[![Rust](https://img.shields.io/badge/rust-2024%20edition-orange.svg)](https://www.rust-lang.org/)

Official GitHub starter template for writing safe, modern GoldSrc engine plugins using [GoldSrc.rs](https://github.com/goldsrc-rs/goldsrc-rs).

## Features

- **Built with modern Rust (Edition 2024)**: Memory-safe, high-performance plugin development.
- **Ergonomic DSL & Macros**: Declarative commands (`#[command]`), lifecycle hooks (`#[on_load]`, `#[on_unload]`), menus, and ECS.
- **GitHub Actions CI/CD**: Preconfigured matrix builds testing both Linux and Windows platforms (`cargo clippy -D warnings`, `cargo test`, and `cargo fmt`).
- **Auto-Formatting Workflow**: Background `fmt.yml` workflow with concurrency guards.
- **Dual Licensing**: MIT and Apache 2.0 open-source licenses.

## Getting Started

### 1. Using GitHub Web Interface
Click the green **"Use this template"** button at the top of the repository to generate your new plugin repository.

### 2. Using `cargo-generate`
```bash
cargo generate goldsrc-rs/goldsrc-template-plugin-rust --name my_awesome_plugin
cd my_awesome_plugin
```

### 3. Using GoldSrc.rs CLI
```bash
goldsrc new my_awesome_plugin --template plugin-rust
```

## Building

Compile release shared libraries (`.so` on Linux, `.dll` on Windows):

```bash
cargo build --release
```

The output artifacts will be located in:
- Linux: `target/release/lib<plugin_name>.so`
- Windows: `target/release/<plugin_name>.dll`

## License

Licensed under either of:

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.
