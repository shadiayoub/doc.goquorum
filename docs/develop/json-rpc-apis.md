---
title: JSON-RPC APIs
description: JSON-RPC APIs
sidebar_position: 2
---

# JSON-RPC Server

Metacces is based on the [Geth Go Ethereum client](https://geth.ethereum.org/) and supports all [standard web3 JSON-RPC APIs](https://geth.ethereum.org/docs/rpc/server). JSON-RPC is supported over HTTP, WebSocket, and Unix Domain Sockets, which are enabled through [command-line options](./connecting-to-a-node.md)

Ethereum JSON-RPC APIs use a namespace system, and methods are grouped into categories depending on their purpose. The general form for a method name is the namespace and the actual method name, separated by an underscore.

In addition to the standard APIs, Metacces adds extra capabilities with to permissioning, privacy, consensus methods, and contracts, all of which are detailed in the [API documentation](../reference/api-methods.md).
