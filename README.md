Build tools for Rust on seL4
============================

This repository contains a set of tools for integrating the `cargo`
build system into CMake projects that build systems on seL4. The tools
in this repository serve a few puroposes, including:

 * building a sysroot containing `libcore` and `liballoc` that can be
	 used as the basis of `#![no_std]` crates,
 * Constructing static libraries via `cargo` that can be linked into C
	 binaries,
 * Constructing static ELF binaries via `cargo`,
 * Linking rust crates with dependency tracking via CMake,
 * Generating rust libraries from C projects files using `bindgen`,
 * Generating C headers from rust projects using `cbindgen`, and
 * Generating documentation for Rust components via `cargo doc`.

In addittion to the above tools, this repository also contains a shim to
generate Rust bindings for `libsel4` using the generated C bindings.

Build dependencies
------------------

In order to build projects using these tools, you must have `cargo`
installed along with it's dependencies. The `cargo` install must also
contain a copy of the `rust-src` component (which is used to build the
sysroot).

You will also need to install `bindgen` and `cbindgen`, these can be
installed using `cargo`.

Including the tools in a CMake project
--------------------------------------

> *TODO*: Add instructions for including the Rust tools

Declaring a crate
-----------------

> *TODO*: Add instructions for declaring a crate in CMake

> *NOTE*: Has flag to specify path to `Cargo.toml`

> *NOTE*: Has flags to indicate which libraries are produced (`CLIB`,
> `CDYLIB`, `RLIB`)

Declaring binary output files
-----------------------------

> *TODO*: Add instructions for declaring binary outputs for a crate

Adding CMake dependencies
-------------------------

> *TODO*: Add instructions for declaring dependencies managed by CMake

> *TODO*: Add instructions for setting environment variables based on
> dependencies

Generating Rust bindings from C
-------------------------------

> *TODO*: Add instructions for generating Rust bindings from C

Generating C bindings from Rust
-------------------------------

> *TODO*: Add instructions for generating C bindings from Rust
