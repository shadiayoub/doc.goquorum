---
title: Account management
description: Managing accounts
sidebar_position: 4
---

# Account/key management

Cryptographic keys are an essential component of a Metacces network. Metacces uses keys to create digital signatures which verify a sender's identity and prevent message tampering. The Privacy Manager uses keys to encrypt private transaction data.

Both Metacces and the Privacy Manager use user-provided asymmetric key pairs. Each key pair consists of a public key and a private key. The public key can be shared freely, but **the private key should never be shared**.

- Metacces derives the account address from the public key by taking the last 20 bytes of its keccak256 hash
- The Privacy Manager uses the public key as an identifier for the target nodes of a private transaction (that is the `privateFor` transaction field)
