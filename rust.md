# Rust入门



## 安装Rust

### Rustup：Rust安装器和版本管理工具

安装 Rust 的主要方式是通过 Rustup 这一工具，它既是一个 Rust 安装器又是一个版本管理工具。

您似乎正在运行 macOS、Linux 或其它类 Unix 系统。要下载 Rustup 并安装 Rust，请在终端中运行以下命令，然后遵循屏幕上的指示。如果您在 Windows 上，请参见 [“其他安装方式”](https://forge.rust-lang.org/infra/other-installation-methods.html)。

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### Rust 是最新的吗？

Rust 的升级非常频繁。如果您安装 Rustup 后已有一段时间，那么很可能您的 Rust 版本已经过时了。运行 `rustup update` 获取最新版本的 Rust。

### Cargo：Rust 的构建工具和包管理器

您在安装 Rustup 时，也会安装 Rust 构建工具和包管理器的最新稳定版，即 Cargo。Cargo 可以做很多事情：

- `cargo build` 可以构建项目
- `cargo run` 可以运行项目
- `cargo test` 可以测试项目
- `cargo doc` 可以为项目构建文档
- `cargo publish` 可以将库发布到 [crates.io](https://crates.io/)。

要检查您是否安装了 Rust 和 Cargo，可以在终端中运行：

```
cargo --version
```

创建新项目

'''

cargo new hello-rust

'''
