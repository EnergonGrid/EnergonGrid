# EPA / Energon Network — Integration Layer

> **Architecture note:** **Energon Network** is the larger on-chain infrastructure. An **Energon Project Adapter (EPA)** is a project-specific adapter created through the Network. EPA is not a synonym for the entire Network.

## Purpose

The Energon Network provides an integration layer for participating projects and services while keeping the immutable core protocol and the separately deployed EVault distinct.

The umbrella EnergonGrid project contains the core protocol, economic components, integration infrastructure, and user-facing interfaces.

## Mainnet component directory

These components and addresses are recorded in the [EnergonGrid README](../README.md) as deployed on **Flare Mainnet (chain ID 14)**.

| Component | Recorded version | Address |
| --- | --- | --- |
| Energon Network | v1.0.0 | `0x6c0bB202a4AF3126E21BbaD6c4D79A8DD41Cc5aC` |
| Energon Node Registry | v2.1.0 | `0x834F79cdDc43CF231bFe7b1abC622ceF7Cbe14a5` |
| Energon NFT System | v1.0.0 | `0xE542801A7F82c5E0D40a02e72EB5d40AB25C067c` |
| Energon NFT Delivery | v1.0.0 | `0xe946d9892E54A7F09e373894e8A478aa793bEcB0` |
| Energon Service Resolution | v1.0.0 | `0xE24b8f0D1a85b567b565322074A0f157EaE6053A` |
| Energon Established Mark | v1.0.0 | `0x28525B92678Bd3AFA5825b45421842bfA46DFdBa` |

The table is a component directory, not a statement that each service has identical privileges or that all are controlled by one contract.

## Network and Project Adapter distinction

The current deployment overview documents this relationship:

- `EnergonNetwork` is a deployed Network contract.
- A project enters the Network through `EnergonNetwork.createNode()`.
- Project Adapters are created by that entry process; there is no single standalone global EPA deployment to list alongside the Network address.
- Individual Project Adapter addresses and configuration should be discovered from the actual creation transaction, emitted events, and current contract state, rather than invented or inferred.

## Separation of responsibility

**Core protocol**  
EON, EnergonCube, and EnergonController define token, identity, and progression rules.

**Economic layer**  
EVault enforces its own reserve, claim, and settlement constraints.

**Integration layer**  
Energon Network and its associated components provide project integration and network service functionality according to their deployed contracts.

**Interfaces**  
The DApp, website, and observers present relevant state; they do not substitute for deployed contract rules.

## Integration documentation to publish with verified source

A dedicated technical reference should include the verified production interfaces/ABIs, `createNode()` parameters, emitted events, Node Registry relationship, adapter discovery, fees and asset flows (if applicable), security assumptions, and real transaction examples.

Only publish those details after comparing them against the deployed source and verified mainnet configuration.

## Source of truth

This document is an architecture map. **The deployed contracts and on-chain state are authoritative** when implementation and documentation differ.

For the umbrella architecture, see [EnergonGrid](../README.md).

For the economic layer, see [EMP / EVault](evault.md).
