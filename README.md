# New Actor Template

Use cargo generate to create a new actor module from this template:

```
cargo generate --git https://github.com/wasmcloud/new-actor-template --branch main
```

Use the `wash` CLI to sign your WebAssembly module after you have created it. The `Makefile` created by this template will sign your module for you with `make build` and `make release`.

## Usage

```
cargo generate --
```

## Requirements

- Rust
- Cargo
- [wash](https://github.com/wasmcloud/wash) - wasmcloud's multi-purpose CLI
- cargo-make to run `cargo make` commands
- wapc-cli for generating rust from widl interface files.
- node.js for wapc-cli

### Installing cargo-make

```
$ cargo install cargo-make
```

### Installing wapc cli

```
$ git clone git@github.com:wapc/cli.git wapc-cli
$ cd wapc-cli
$ npm install -g .
```

### Note

`cargo make` will use keys that are generated _locally_ for you. Once you move this actor into a pipeline toward a production deployment, you will want to explicitly specify the key locations and disable key generation in `wash` with the `--disable-keygen` option.
