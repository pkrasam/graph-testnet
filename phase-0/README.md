### my Notes

Thank you for creating an opportunity for me/us to participate in this amazing testnet phase of the Graph protocol.

I am super excited, eager to learn and contribute throughout the 5 phases.

I had some speed bumps in the beginning, but I believe the community is coming together really well and helping each other.

**Highlights:**
- 1st to get turbo-geth archive node fully synced in < 42 hrs for both mainnet and rinkeby testnet
- share the fully synced 650 GB ethereum mainnet database with the community
- completed installing the graph indexer-node, graph query-node, postgres database, grafana, prometheus on bare metal
- deployed all 4 sub-graphs
- indexed all 4 sub-graphs
- tested all 7 queries from test harness individually and they work
- ready for phase 1

**Feedback:**
- during the 3 week period for each phase, it might be helpful to have an AMA session w/ the graph team so we can learn faster and focus on getting more done in the testnet phase

**Endpoints:**

indexer: http://indexer.pkrasam.co

grafana: http://grafana.pkrasam.co

prometheus: http://prometheus.pkrasam.co


[jannis/gravity](http://indexer.pkrasam.co/subgraphs/name/jannis/gravity/graphql)

[molochventures/moloch](http://indexer.pkrasam.co/subgraphs/name/molochventures/moloch/graphql)

[uniswap/uniswap-v2](http://indexer.pkrasam.co/subgraphs/name/uniswap/uniswap-v2/graphql)

[synthetixio-team/synthetix](http://indexer.pkrasam.co/subgraphs/name/synthetixio-team/synthetix/graphql)


**Queries:**
[q1, q2, q3, q4, q5, q6, q7]

```
QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9,{ votes { id } }
QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9,{ proposals { id } }
QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9,{ members { id } }
QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9,{ members { id votes(where: {timestamp_gt: "1234"}) { id proposalIndex } } }
QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP,{ uniswapFactories(first: 5) { id pairCount totalVolumeUSD } tokens(first: 5) { id symbol name decimals } }
QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP,{ users(orderBy: usdSwapped) { id usdSwapped } }
QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP,{ swaps(where: { timestamp_gt: "10000"}) { pair { token0 { name } token1 { name } } } }
```

**Results:**
[r1, r2, r3, r4, r5, r6, r7]

r1
```
{
  "data": {
    "votes": [
      {
        "id": "0x0039f22efb07a647557c7c5d17854cfd6d489ef3-112"
      },
      {
        "id": "0x0b916095200313900104bacfc288462682c38700-102"
      },
      {
        "id": "0x0b916095200313900104bacfc288462682c38700-108"
      },
      ...
```
r2
```
{
  "data": {
    "proposals": [
      {
        "id": "0"
      },
      {
        "id": "1"
      },
      {
        "id": "10"
      },
      ...
```
r3
```
{
  "data": {
    "members": [
      {
        "id": "0x0039f22efb07a647557c7c5d17854cfd6d489ef3"
      },
      {
        "id": "0x02cb3c150bedca124d0ae8cccb72fefbe705c953"
      },
      {
        "id": "0x04576eb9aff2be4122d1ba870eea8db4573a97d9"
      },
      ...
```
r4
```
{
  "data": {
    "members": [
      {
        "id": "0x0039f22efb07a647557c7c5d17854cfd6d489ef3",
        "votes": [
          {
            "id": "0x0039f22efb07a647557c7c5d17854cfd6d489ef3-112",
            "proposalIndex": "112"
          }
        ]
      },
      {
        "id": "0x02cb3c150bedca124d0ae8cccb72fefbe705c953",
        "votes": []
      },
      {
        "id": "0x04576eb9aff2be4122d1ba870eea8db4573a97d9",
        "votes": []
      },
      ...
```
r5
```
{
  "data": {
    "tokens": [
      {
        "decimals": "0",
        "id": "0x0000000000004946c0e9f43f4dee607b0ef1fa1c",
        "name": "Chi Gastoken by 1inch",
        "symbol": "CHI"
      },
      {
        "decimals": "18",
        "id": "0x0000000000085d4780b73119b644ae5ecd22b376",
        "name": "TrueUSD",
        "symbol": "TUSD"
      },
      {
        "decimals": "2",
        "id": "0x0000000000b3f879cb30fe243b4dfee438691c04",
        "name": "Gastoken.io",
        "symbol": "GST2"
      },
      ...
```
r6
```
{
  "data": {
    "users": [
      {
        "id": "0x0000000000000000000000000000000000000000",
        "usdSwapped": "0"
      },
      {
        "id": "0x000206732258d7511fa624127228e6a032718e62",
        "usdSwapped": "0"
      },
      {
        "id": "0x0006e4548aed4502ec8c844567840ce6ef1013f5",
        "usdSwapped": "0"
      },
      ...
```
r7
```
{
  "data": {
    "swaps": [
      {
        "pair": {
          "token0": {
            "name": "UniBright"
          },
          "token1": {
            "name": "Wrapped Ether"
          }
        }
      },
      {
        "pair": {
          "token0": {
            "name": "6ix9ine Chain"
          },
          "token1": {
            "name": "Wrapped Ether"
          }
        }
      },
      {
        "pair": {
          "token0": {
            "name": "UniBright"
          },
          "token1": {
            "name": "Wrapped Ether"
          }
        }
      },
      ...
```
