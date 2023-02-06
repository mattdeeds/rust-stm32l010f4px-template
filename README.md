# `rust-stm32l010f4px-template`

> A template for building applications for ARM Cortex-M0 stm32l010f4 microcontroller

## Dependencies

To build embedded programs using this template you'll need:

- [Rust](https://www.rust-lang.org/tools/install)

- The arm-none-eabi compiler toolchain

- The `cargo generate` subcommand. [Installation
  instructions](https://github.com/ashleygwilliams/cargo-generate#installation).

- `rust-std` components (pre-compiled `core` crate) for the ARM Cortex-M
  targets. Run:

``` console
rustup target add thumbv6m-none-eabi
```

- [cargo-flash](https://probe.rs/) to run examples on target hardware.
``` consol 
cargo install cargo-flash
```

## Using this template


1. Instantiate the template.

``` console
$ cargo generate --git https://github.com/mattdeeds/rust-stm32l010f4px-template
 Project Name: app
 Creating project called `app`...
 Done! New project created /tmp/app

$ cd app
```

2. Build
``` console
cargo build --release
```

3. Build and flash 
``` console
cargo flash --release --chip STM32L010F4Px
```