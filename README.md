# MiniGrep

[![Rust](https://img.shields.io/badge/Rust-2024%20edition-orange)](https://www.rust-lang.org/)
[![Cargo](https://img.shields.io/badge/Build-Cargo-orange)](https://doc.rust-lang.org/cargo/)
[![Dependencies](https://img.shields.io/badge/Dependencies-0-blue)](https://crates.io/)
[![Tests](https://img.shields.io/badge/Tests-cargo%20test-green)](https://doc.rust-lang.org/cargo/commands/cargo-test.html)

MiniGrep is a small command-line text search tool written in Rust. It searches
each line of a text file and prints the lines that contain a given query.

This project was created as a hands-on introduction to Rust.

## Requirements

- [Rust](https://www.rust-lang.org/tools/install) and Cargo

Check that Rust is installed:

```bash
rustc --version
cargo --version
```

## Usage

Run MiniGrep with a query and a file path:

```bash
cargo run -- <query> <file>
```

For example:

```bash
cargo run -- nobody poem.txt
```

The command prints every line containing `nobody`.

### Case-insensitive search

Set the `IGNORE_CASE` environment variable to enable case-insensitive
matching:

```bash
IGNORE_CASE=1 cargo run -- rust poem.txt
```

The value of `IGNORE_CASE` is not important; its presence enables the option.

## Development

Build the project:

```bash
cargo build
```

Run the test suite:

```bash
cargo test
```

Run the compiled binary directly:

```bash
cargo run -- <query> <file>
```

## Resources

- [The Rust Book: An I/O Project](https://doc.rust-lang.org/book/ch12-00-an-io-project.html)
