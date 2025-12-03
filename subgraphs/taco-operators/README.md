# TACo operators subgraph

The Threshold Staking subgraph tracks TACo operators activity on
TACoChildApplication contract.

It monitors TACoChildApplication contract on Polygon mainnet `0xFa07aaB78062Fac4C36995bF28F6D677667973F5`.

The subgraph, when deployed, provides a queryable GraphQL interface that exposes
comprehensive data about TACo operators: what is the operator address, if they
have been confirmed and when.

## Query URL

None.

## Developing and deploying

Please make sure you have the following prerequisites installed on your machine:

- [Node.js](https://nodejs.org) ^18.19.0
- [Yarn](https://yarnpkg.com) ^1.22.21

To deploy the subgraph on Goldsky, it is needed to install [Goldsky CLI](https://docs.goldsky.com/subgraphs/deploying-subgraphs#install-goldskys-cli-and-log-in):

`npm install -g @goldskycom/cli`

An API key is needed for the project.

```bash
yarn codegen
yarn build
goldsky subgraph deploy taco-operators/<version>
```

To see the subgraph logs on Goldsky:

```bash
goldsky subgraph log taco-operators/0.0.1 \
  --format pretty --since 3h --filter warn
```

### Run unit tests

The recommended way to run tests is using a Docker container. It is required to
have [Docker installed](https://docs.docker.com/desktop/).

To run the tests, just execute:

```bash
yarn test
```

Tests can also be run in the local environment, more info in
[Unit Testing Framework](https://thegraph.com/docs/en/developing/unit-testing-framework/).
