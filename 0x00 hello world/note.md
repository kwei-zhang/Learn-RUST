The `main` function is special: it is always the first code that runs in every executable Rust program.
`println!` calls a `Rust macro`. If it had called a function instead, it would be entered as `println` (without the !).

Rust is an `ahead-of-time` compiled language, meaning you can compile a program and give the executable to someone else, and they can run it even without having Rust installed.

---

Cargo is Rust’s build system and package manager. By running 
```
cargo new hello_cargo
cargo new --vcs=git hello_cargo /* generates gitignore */
```
You will see a file in TOML (Tom’s Obvious, Minimal Language) format, which is Cargo’s configuration format.

The first line, `[package]`, is a section heading that indicates that the following statements are configuring a package.

The last line, `[dependencies]`, is the start of a section for you to list any of your project’s dependencies. In Rust, packages of code are referred to as crates.

## Build and run project with Cargo

By running following command
```
cargo build
./target/debug/hello_cargo
OR
cargo run 
```
Running `cargo build` for the first time also causes Cargo to create a new file at the top level: `Cargo.lock`. This file keeps track of the exact versions of dependencies in your project.

Cargo also provides a command called `cargo check`. This command quickly checks your code to make sure it compiles but doesn’t produce an executable.