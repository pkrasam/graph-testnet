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


**Additional Tests:**

url-hc1
```
http://indexer.pkrasam.co/index-node/graphql/playground?query=%7B%0A%20%20indexingStatuses(subgraphs%3A%20%5B%22QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9%22%2C%20%22Qme2hDXrkBpuXAYEuwGPAjr6zwiMZV4FHLLBa3BHzatBWx%22%2C%20%22QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP%22%2C%20%22QmbeDC4G8iPAUJ6tRBu99vwyYkaSiFwtXWKwwYkoNphV4X%22%5D)%20%7B%0A%20%20%20%20health%0A%20%20%20%20synced%0A%20%20%20%20subgraph%0A%20%20%20%20fatalError%20%7B%0A%20%20%20%20%20%20message%0A%20%20%20%20%7D%0A%20%20%20%20chains%20%7B%0A%20%20%20%20%20%20network%0A%20%20%20%20%20%20chainHeadBlock%20%7B%0A%20%20%20%20%20%20%20%20number%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20latestBlock%20%7B%0A%20%20%20%20%20%20%20%20number%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20lastHealthyBlock%20%7B%0A%20%20%20%20%20%20%20%20number%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D
```

query-hc1
```
{
  indexingStatuses(subgraphs: ["QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9", "Qme2hDXrkBpuXAYEuwGPAjr6zwiMZV4FHLLBa3BHzatBWx", "QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP", "QmbeDC4G8iPAUJ6tRBu99vwyYkaSiFwtXWKwwYkoNphV4X"]) {
    health
    synced
    subgraph
    fatalError {
      message
    }
    chains {
      network
      chainHeadBlock {
        number
      }
      latestBlock {
        number
      }
      lastHealthyBlock {
        number
      }
    }
  }
}
```
results-hc1
```
{
  "data": {
    "indexingStatuses": [
      {
        "chains": [
          {
            "chainHeadBlock": {
              "number": "10703663"
            },
            "lastHealthyBlock": null,
            "latestBlock": {
              "number": "10703663"
            },
            "network": "mainnet"
          }
        ],
        "fatalError": null,
        "health": "healthy",
        "subgraph": "QmbeDC4G8iPAUJ6tRBu99vwyYkaSiFwtXWKwwYkoNphV4X",
        "synced": true
      },
      {
        "chains": [
          {
            "chainHeadBlock": {
              "number": "10703663"
            },
            "lastHealthyBlock": null,
            "latestBlock": {
              "number": "6856689"
            },
            "network": "mainnet"
          }
        ],
        "fatalError": null,
        "health": "healthy",
        "subgraph": "Qme2hDXrkBpuXAYEuwGPAjr6zwiMZV4FHLLBa3BHzatBWx",
        "synced": false
      },
      {
        "chains": [
          {
            "chainHeadBlock": {
              "number": "10703663"
            },
            "lastHealthyBlock": null,
            "latestBlock": {
              "number": "10703663"
            },
            "network": "mainnet"
          }
        ],
        "fatalError": null,
        "health": "healthy",
        "subgraph": "QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9",
        "synced": true
      },
      {
        "chains": [
          {
            "chainHeadBlock": {
              "number": "10703663"
            },
            "lastHealthyBlock": null,
            "latestBlock": {
              "number": "10251057"
            },
            "network": "mainnet"
          }
        ],
        "fatalError": null,
        "health": "healthy",
        "subgraph": "QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP",
        "synced": false
      }
    ]
  }
}
```

url-hc2
```
http://prometheus.pkrasam.co/federate?match[]=subgraph_query_execution_time_count&match[]=subgraph_count&match[]=QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP_sync_total_secs&match[]=Qme2hDXrkBpuXAYEuwGPAjr6zwiMZV4FHLLBa3BHzatBWx_sync_total_secs&match[]=QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9_sync_total_secs
```
results-hc2
```
# TYPE QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9_sync_total_secs untyped
QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9_sync_total_secs{instance="172.21.0.1:8140",job="thegraph"} 0 1598143894622
# TYPE QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP_sync_total_secs untyped
QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP_sync_total_secs{instance="172.21.0.1:8140",job="thegraph"} 70340.89442826265 1598143894622
# TYPE Qme2hDXrkBpuXAYEuwGPAjr6zwiMZV4FHLLBa3BHzatBWx_sync_total_secs untyped
Qme2hDXrkBpuXAYEuwGPAjr6zwiMZV4FHLLBa3BHzatBWx_sync_total_secs{instance="172.21.0.1:8140",job="thegraph"} 69984.2894548387 1598143894622
# TYPE subgraph_count untyped
subgraph_count{instance="172.21.0.1:8140",job="thegraph"} 3 1598143894622
subgraph_count{instance="172.21.0.1:8040",job="thegraph"} 1 1598143903200
# TYPE subgraph_query_execution_time_count untyped
subgraph_query_execution_time_count{instance="172.21.0.1:8040",job="thegraph",subgraph_deployment="QmTXzATwNfgGVukV1fX2T6xw9f6LAYRVWpsdXyRWzUR2H9"} 2874 1598143903200
subgraph_query_execution_time_count{instance="172.21.0.1:8040",job="thegraph",subgraph_deployment="subgraphs"} 11 1598143903200
subgraph_query_execution_time_count{instance="172.21.0.1:8040",job="thegraph",subgraph_deployment="QmXKwSEMirgWVn41nRzkT3hpUBw29cp619Gx58XW6mPhZP"} 2059 1598143903200
```
