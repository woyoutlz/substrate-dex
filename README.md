# Dex demo build by substrate

## Build

Install Rust:

```bash
curl https://sh.rustup.rs -sSf | sh
```

Install required tools:

```bash
./scripts/init.sh
```

Build Wasm and native code:

```bash
cargo build
```

## Run

### Single node development chain

You can start a development chain with:

```bash
cargo run -- --dev
```

Detailed logs may be shown by running the node with the following environment variables set: `RUST_LOG=debug RUST_BACKTRACE=1 cargo run -- --dev`.

### Play with the dex

Please refer the client/transactions-api to see how to play with the dex chain. You can:

- issue the token
- transfer the token
- create the trade pair
- create the limit order
- cancel the limit order

Also, you can play with it by [polkadotjs](https://github.com/polkadot-js/apps) wallet frontend with:

```bash
git clone https://github.com/polkadot-js/apps
cd apps
yarn
yarn start
```

Then open the link [http://localhost:3000/#/?rpc=ws://127.0.0.1:9944](http://localhost:3000/#/?rpc=ws://127.0.0.1:9944)

### About next step

- Will provide a full-feature dex front-end build with polkadotjs
- Will upgrade to substrate 2.0 whenever it released