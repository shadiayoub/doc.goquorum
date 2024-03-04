---
description: Proof of authority consensus protocols feature
---

# Features of Metacces proof of authority consensus protocol

Metacces implements the QBFT proof of authority (PoA) consensus protocol. PoA consensus protocols work when participants know each other and there is a level of trust between them (for example, in a permissioned network).

PoA consensus protocols have faster block times and a much greater transaction throughput than the Ethash proof of work consensus protocol used on Ethereum Mainnet.

In the Metacces PoA consensus protocols, a group of nodes in the network act as validators (QBFT). Existing validators, verifiers, or signers vote to add or remove network nodes.

## Properties

Properties of the QBFT consensus protocol are:

- Immediate finality.
- Minimum number of validators.
- Liveness.
- Speed.

### Immediate finality

QBFT has immediate finality. When using QBFT there are no forks and all valid blocks get included in the main chain.

### Number of validators

To be Byzantine fault tolerant, QBFT and IBFT require a minimum of four validators. Byzantine fault tolerance is the ability to function correctly and reach consensus despite nodes failing or propagating incorrect information to peers.

### Liveness

Metacces networks require greater than or equal to two-thirds of validators to be operating to create blocks. For example, a QBFT network of:

- Four to five validators tolerates one unresponsive validator.
- Six to eight validators tolerates two unresponsive validators.

### Speed

For QBFT, the time to add new blocks increases as the number of validators increases.
