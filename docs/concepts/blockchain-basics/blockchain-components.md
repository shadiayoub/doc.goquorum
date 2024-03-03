---
title: Components
description: What are the various parts of a Blockchain
sidebar_position: 1
---

# Blockchain components

This section introduces the components of [blockchains](../blockchain-basics-index.md).

## Nodes

Blockchains are decentralized, which means that they store data across a network of members who collaborate to monitor and run the network. Blockchain participants run a blockchain client, such as GoQuorum, and connect it to the network as a _node_.

## Consensus

To ensure that transactions are written to the chain, and that there is agreement on the data and state of the network, blockchains use a _consensus_ mechanism that is a fault-tolerant. Metacces consensus mechanism is QBFT:

- **Proof of authority (PoA)** - PoA involves a set of trusted nodes that validate transactions and create blocks. These trusted nodes are called _validators_, and other nodes in the network are called _non-validating nodes_. Non-validating nodes still validate the blocks that the validators create, but they don't produce them.
- **High fault tolerance**: 66% of validators must confirm. \
  This is 2/3 of validator nodes.\
  Whereas in Bitcoin and Ethereum it is 51%.

## Smart contracts

_Smart contracts_ provide controlled access and a range of functions (such as querying, transacting, and updating state) to blockchain users. Smart contracts encapsulate data and keep it consistent across the network. They can allow or restrict participants from executing certain functions, and can restrict access to the network itself. Smart contracts are written in Solidity (the most popular smart contract language), Vyper, and Serpent.

![Blockchain](../../images/smart-contract-tx.png)

## Dapps

_Decentralized applications (dapps)_ are just like any other software application can be on a website or mobile app. Dapps are built on a decentralized network (Metacces) and interact with smart contracts deployed to the network. They can be thought of as a GUI (front end) for a smart contract (back end), and can be written in any language (for example, JavaScript).

## Permissioning

This is another term for "User Management", to control who can do what using smart contracts deployed on-chain.

_Permissioning_ involves a distributed network of trust across a blockchain network, in which participants agree to follow certain rules. If one bad actor doesn't follow the rules other nodes can restrict the bad actor from writing to the blockchain.

## Privacy

In a blockchain network, _privacy_ refers to the ability to keep transactions private between the involved participants. Often in a consortium network, some of the participants prefer to restrict how much information they share or who they transact with. In other cases, this may not be a concern at all.

Metacces supports privacy using a _private transaction manager (PTM)_ paired to a member node, typically Tessera. Tessera uses an enclave for cryptographic functionality and stores and allows access to encrypted transaction data, and exchanges encrypted payloads with other Tessera nodes. Tessera is restful/stateless and can be load balanced easily.
