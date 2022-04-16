# Rust Learning

Reading *The Rust Programming Language* by Steve Klabnik and Carol Nichols

## Ch 01 Getting Started

```rust
fn main() {
    println!("Hello, world!")
}
```

`main()` always runs first in a Rust program.

Wrap function body in curly brackets.

`rustfmt` can autoformat code (like Black for python).

The `!` in `println!` denotes that a *macro* is being called. Functions are called without the exclamation point.

To compile:
```bash
$ rustc main.rs
```

`cargo` is Rust's build system and package manager.

Create a binary application with cargo:
```bash
$ cargo new hello_cargo --bin
$ ls hello_cargo
hello_cargo/
├── Cargo.toml
└── src
    └── main.rs
$ cd hello_cargo
$ cargo build
$ tree
.
├── Cargo.lock
├── Cargo.toml
├── src
│   └── main.rs
└── target
    ├── CACHEDIR.TAG
    └── debug
        ├── build
        ├── deps
        │   ├── hello_cargo-a714c16e90f17bf5
        │   └── hello_cargo-a714c16e90f17bf5.d
        ├── examples
        ├── hello_cargo
        ├── hello_cargo.d
        └── incremental
            └── *
$ ./target/debug/hello_cargo 
Hello, world!
$ cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
     Running `target/debug/hello_cargo`
Hello, world!

```

`cargo check` will check code without creating binaries.

`cargo run` will run code and rebuild if necessary.

`cargo build --release` will build code with optimizations. Adds release directory to project.

## Ch 02 Programming a Guessing Game


