---
title: Architecture
description: Overview of Metacces architecture
sidebar_position: 2
---

# Architecture

The following diagram outlines the Metacces high-level architecture.

![GoQuorum Architecture diagram](../images/Quorum%20Design.png)

## Differences from geth

Metacces is a lightweight fork of geth using GoQuorum, which is updated as geth releases occur.

Metacces includes the following changes to geth:

- Consensus is achieved with the QBFT consensus protocols instead of proof of work.
- The block generation logic is changed to replace the `global state root` check with a `global public state root` check.
- The block validation logic is changed to replace the `global state root` in the block header with the `global public state root`.
- The State Patricia trie is split into two: a public state trie and a private state trie.
- Block validation logic is changed to handle private transactions.
- Transaction creation is changed to allow for replacing transaction data with encrypted hashes to preserve private data where required.
