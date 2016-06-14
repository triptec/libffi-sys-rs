# libffi-sys-rs: Low-level Rust bindings for [libffi](https://sourceware.org/libffi/)

[![Build Status](https://travis-ci.org/tov/libffi-sys-rs.svg?branch=master)](https://travis-ci.org/tov/libffi-sys-rs)
[![Crates.io](https://img.shields.io/crates/v/libffi-sys.svg?maxAge=2592000)](https://crates.io/crates/libffi-sys)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE-MIT)
[![License: Apache 2.0](https://img.shields.io/badge/license-Apache_2.0-blue.svg)](LICENSE-APACHE)

The C libffi library provides two main facilities: assembling calls
to functions dynamically, and creating closures that can be called
as ordinary C functions. This is an undocumented wrapper, generated
by bindgen, intended as the basis for higher-level bindings, but you
can see the [C libffi
documentation](http://www.atmark-techno.com/~yashi/libffi.html).

See [the libffi crate](https://crates.io/crates/libffi/) for a
higher-level API.

## Usage

It’s [on crates.io](https://crates.io/crates/libffi-sys), but before you
build it, make sure you have the dependencies installed first:

  - An up-to-date version of C [libffi](https://sourceware.org/libffi/)
    Version 3.2.1 is known to work. Earlier versions, such as the
    versions that come with Mac OS and Fedora, are known not to; neither
    will the version installed by Homebrew (3.0.13).

  - [`pkg-config`](https://www.freedesktop.org/wiki/Software/pkg-config/),
    which you probably already have if you’re on Linux. For Mac users,
    the version installed by Homebrew is up to date. (I don’t know how
    this works on Windows; contact me if you’d like to help figure it
    out.)

Then add

```toml
[dependencies]
libffi-sys = "@VERSION@"
```

to your `Cargo.toml` and

```rust
extern crate libffi_sys;
```

to your crate root.