# Threshold Network staking subgraphs

This repository contains the code of subgraphs to track Threshold Network
staking and TACo Application events.

Subgraphs are open APIs to query data from networks like Ethereum and IPFS. The
data is indexed by [The Graph](https://thegraph.com) decentralized protocol.

## Development

Please make sure you have the following prerequisites installed on your machine:

- [Node.js](https://nodejs.org) ^18.19.0
- [Yarn](https://yarnpkg.com) ^1.22.21

Install the root package to set up the linter and formatting tools.

```bash
yarn install
```

This repo is organized in folders that contain each subgraph development. Each
of them is a NPM package with its own dependencies and contains a README file.

You should navigate to the subgraph's folder of interest and follow the README
instructions.

```bash
cd subgraphs/threshold-staking/
yarn install
```
