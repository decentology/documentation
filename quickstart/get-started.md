---
description: >-
  In this section of the QuickStart guide, you'll learn how to start working on
  your decentralized application.
---

# Get Started

## **Pre-requisites**

**In order to develop and build "My Dapp,"** the following pre-requisites must be installed:

* [NodeJS](https://nodejs.org/en/download/)
* [Yarn](https://classic.yarnpkg.com/en/docs/install) (DappStarter uses [Yarn Workspaces](https://classic.yarnpkg.com/en/docs/workspaces))
* For Flow only:&#x20;
  * [Flow CLI](https://docs.onflow.org/docs/cli) (after installation run `flow cadence install-vscode-extension` to enable code highlighting for Cadence files)
* For Solana only:&#x20;
  * [Solana CLI Tools](https://docs.solana.com/cli/install-solana-cli-tools)
  * Rust (see "[Dependency Guides](https://docs.decentology.com/quickstart/get-started#dependency-guides)" at the end for help installing)

## **Installation**

Using a terminal (or command prompt), change to the folder containing the project files and type: `yarn`. This will fetch all required dependencies. The process will take 1-3 minutes and while it’s in progress, you can move on to the next step.

### Yarn Errors

You might see failures related to the `node-gyp` package when Yarn installs dependencies. These failures occur because the node-gyp package requires certain additional build tools to be installed on your computer. Follow the [instructions](https://www.npmjs.com/package/node-gyp) for adding build tools and then try running `yarn` again.

## **Build, Deploy and Test**

Using a terminal (or command prompt), change to the folder containing the project files and type: `yarn start` This will run all the dev scripts in each project package.json.

To view your dapp, open your browser to [http://localhost:5000](http://localhost:5000) for the DappStarter Workspace.

## Dependency Guides

This section contains installation guides for common dev environments.

### Rust (Solana)

(Source: Solana) We suggest that you install Rust using the 'rustup' tool. Rustup will install the latest version of Rust, Cargo, and the other binaries.

Follow the instructions at [Installing Rust](https://www.rust-lang.org/tools/install).

For Mac users, Homebrew is also an option. The Mac Homebrew command is `brew install rustup` and then `rustup-init`. See [Mac Setup](https://sourabhbajaj.com/mac-setup/Rust/) & [Installing Rust](https://www.rust-lang.org/tools/install) for more details.

After installation, you should have `rustc`, `cargo`, & `rustup`. You should also have `~/.cargo/bin` in your PATH environment variable.

## Other Scripts

If you prefer to run scripts individually, the order is:

### Smart Contract

`lerna run deploy --scope=@trycrypto/dappstarter-dapplib --stream` to compile contracts/\*.sol files, deploy them to the blockchain.

### Dapp

Run the dapp in a separate terminal. You must have run npm run deploy for the dapp to see the most recent smart contract changes.

`lerna run dev --scope=@trycrypto/dappstarter-client --stream` runs the dapp on [http://localhost:5001](http://localhost:5001) using webpack dev server

### Server

Run the server in a separate terminal. You must have run npm run deploy for the dapp to see the most recent smart contract changes.

`lerna run dev --scope=@trycrypto/dappstarter-server --stream` runs NodeJS server app on port 5002 with NestJS

### Testing

test-config.js contains settings used by test scripts

Run tests using `lerna run test [test file] --scope=@trycrypto/dappstarter-dapplib --stream`

### Production Builds

DappStarter currently does not provide blockchain migration scripts to be used in production. However, here are the scripts for generating production builds:

`lerna run build:prod` generates dapp bundle for production.\
