# `rust-stm32l010f4px-template`

> A template for building applications for ARM Cortex-M0 stm32l010f4 microcontrollers

Based off of [cortex-m-quickstart](https://github.com/rust-embedded/cortex-m-quickstart) and [stm32l0xx-hal](https://github.com/stm32-rs/stm32l0xx-hal)

## Dependencies

To build embedded programs using this template you'll need:

- [rustup](https://rustup.rs/)

- The arm-none-eabi compiler toolchain
  - On Ubuntu or Debian: apt-get install gcc-arm-none-eabi binutils-arm-none-eabi
  - On MacOS, grab a pre-built toolchain from the homebrew-arm repo

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

# License

This template is licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or
  http://www.apache.org/licenses/LICENSE-2.0)

- MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.
