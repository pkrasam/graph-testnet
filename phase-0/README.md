### my Notes

Thank you for creating an opportunity for me/us to participate in this amazing testnet phase of the Graph protocol.

I am super excited, eager to learn and contribute throughout the 5 phases.

I had some speed bumps in the beginning, but I believe the community is coming together really well and helping each other.

Highlights:
- 1st to get turbo-geth archive node fully synced in < 42 hrs for both mainnet and rinkeby testnet
- share the fully synced 650 GB ethereum mainnet database with the community
- tinker w/ installing the graph node, postgres database, metrics, etc. on a bare metal
 
Next Steps:
- setting up infrastructure on a bare metal using kubernetes (k3s), rancher, helm

Feedback:
- during the 3 week period for each phase, it might be helpful to have an AMA session w/ the graph team so we can learn faster and focus on getting more done in the testnet phase

Endpoint:
```
default: 35.238.171.161
index: 34.68.144.237
query: 34.70.60.47
```

GCP Installation Outputs:
C0
```
kubectl config use-context $(kubectl config get-contexts --output='name' | grep $indexer)
```
O0
```
Switched to context "gke_w3m-graph_us-central1-a_w3m-indexer".
```

