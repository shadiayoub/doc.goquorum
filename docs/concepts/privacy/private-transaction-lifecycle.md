---
title: Private transaction lifecycle
description: Private transaction flow
sidebar_position: 4
---

# Private transaction lifecycle

This topic illustrates the high-level lifecycle of normal [private transactions](private-and-public.md#private-transactions) and [privacy marker transactions (PMTs)](privacy-marker-transactions.md).

In both examples, participants A and B are party to the transaction and participant C is not.

## Normal private transactions

![Private transaction flow](../../images/PrivateTxnFlow.png)

1. Participant A sends a private transaction to their Metacces node A.
2. Metacces serializes the private transaction `data` value to JSON and sends it to Tessera node A with participant details.
3. Tessera encrypts the `data` and distributes it to transaction participants.
4. Tessera returns the hash of the encrypted `data` to Metacces node A. Metacces replaces the private transaction `data` value with the hash. Metacces signs the private transaction and sets the `v` value to `37` or `38` to mark the transaction as private.
5. Metacces distributes the private transaction throughout the network.
6. All nodes can see the transaction. Only transaction participants (participants A and B) can get the decrypted data from Tessera and execute the transaction.

## Privacy marker transactions

![Privacy marker transaction flow](../../images/PMTFlow.png)

1. Participant A sends a private transaction to their Metacces node A.

2. Metacces serializes the private transaction `data` value to JSON and sends it to Tessera node A with participant details.

3. Tessera encrypts the `data` and distributes it to transaction participants.

4. Tessera returns the hash of the encrypted `data` to Metacces node A. Metacces creates a public PMT with the `data` field set to the hash. Metacces signs the PMT.

5. Metacces distributes the PMT throughout the network. All nodes can see the PMT.

   The PMT is processed in the same way as a standard public transaction. Since the PMT's `to` value is the address of the privacy precompile contract, that contract is called.

6. Metacces nodes B and C call the privacy precompile with the PMT `data`.

7. Metacces attempts to retrieve the decrypted private transaction from Tessera using the publicly available hash from the PMT.

8. Action depends on whether the node is a transaction participant:

   1. Participant: Metacces gets the decrypted `data` of the private transaction from Tessera and the privacy precompile executes the private transaction.

   2. Non-participant: No private transaction is found, so the privacy precompile returns immediately.
