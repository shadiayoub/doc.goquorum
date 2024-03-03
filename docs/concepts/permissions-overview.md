---
title: Permissioning
description: Permissioning overview
sidebar_position: 8
---

# Permissioning

Metacces uses enhanced network permissioning for user management.

## Enhanced network permissioning

The enhanced network permissioning model caters to enterprise-level needs by using smart contracts. It has significant flexibility to manage nodes, accounts, and account-level access controls.&#x20;

The permissioning rules are applied both at the time of transaction entry and block minting with respect to the data stored in the permissioning contracts.

### Key definitions

![permissions mode](../images/PermissionsModel.png)

- Network - A set of interconnected nodes representing an enterprise blockchain. The network comprises a group of organizations. The network administrator accounts defined at the network level can propose and approve new organizations to join the network, and can assign an account as an organization administrator.
- Organization - A set of roles, Ethereum accounts, and nodes having a variety of permissions to interact with the network. The organization administrator can create roles, create sub-organizations, assign roles to its accounts, and add any other node that is part of the organization. The organization administrator can assign an account as a sub-organization administrator.
- Sub-organization - A sub-group within an organization, corresponding to business needs. A sub-organization can have its own set of roles, accounts, and sub-organizations.
- Account - An externally-owned Ethereum account. The access rights of an account are derived based on the role assigned to it. The account can transact via any node linked to its sub-organization or at the organization level.
- Voter - An account capable of voting for a certain action.
- Role - A named job function in an organization.
- Node - A `geth` node that is part of the network and belongs to an organization or sub-organization.
