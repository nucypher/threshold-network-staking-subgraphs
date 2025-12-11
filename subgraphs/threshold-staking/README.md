# Threshold-staking subgraph

The Threshold Staking subgraph tracks staking activity and governance data for
the Threshold Network on Ethereum mainnet.

It monitors three main smartcontracts:

- Token Staking on Ethereum mainnet `0x01B67b1194C75264d06F808A921228a95C765dd7`:
staking operations (stakes, top-ups, unstaking, and authorizations to applications).
- Threshold Token on Ethereum mainnet `0xCdF7028ceAB81fA0C6971208e83fa7872994beE5`:
traking DAO voting power delegations.
- TACo Application on Ethereum mainnet `0x347CC7ede7e5517bD47D20620B2CF1b406edcF07`:
monitoring TACo operator bonding and commitments.

The subgraph, when deployed, provides a queryable GraphQL interface that exposes
comprehensive data about staking providers, their stake amounts and history,
application authorizations, voting delegations for both Stake and Tokenholder
DAOs, minimum stake requirements, and TACo operator information.

## Query URL

`https://api.goldsky.com/api/public/project_cmgzo6cgq00lc5np2dwaycfdl/subgraphs/threshold-staking/0.0.3/gn`

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
goldsky subgraph deploy threshold-staking/<version>
```

To see the subgraph logs on Goldsky:

```bash
goldsky subgraph log threshold-staking/0.0.1 \
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
