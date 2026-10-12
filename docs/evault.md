# EMP / Energon EVault — Economic Layer

> **Architecture note:** The **Energon Management Protocol (EMP)** is an Energon protocol document/framework. **Energon EVault** is a deployed smart-contract component of the ecosystem. The terms are related, but they are not interchangeable.

## Purpose

EVault provides a separately deployed economic layer for conditional exchanges and claims under predefined on-chain constraints. It is not the Energon core protocol, a replacement for EnergonController, or an administrator over Guardian identity.

This layer is intended to make reserve, eligibility, timing, budget, and settlement conditions inspectable rather than discretionary.

## Mainnet deployment

| Component | Version recorded in the ecosystem README | Flare Mainnet address |
| --- | --- | --- |
| Energon EVault | v5.8.0 | `0x4f4C84321f83f77e95359e16f472b130Ed15EF04` |

Network: **Flare Mainnet (chain ID 14)**.

This record identifies the deployed contract. Do not treat this architecture document as a replacement for the verified contract source, ABI, constructor parameters, or on-chain state.

## Responsibilities and boundaries

- **EVault:** enforces its own on-chain economic rules, eligibility checks, reserve constraints, claim lifecycle, and payout limitations as implemented in the deployed contract.
- **EMP:** documents the intended management and economic framework; documentation does not supersede contract execution.
- **Energon core:** EON supply, EnergonCube ownership/coherence, genesis, and EnergonController progression remain independent and are governed by their deployed contracts.
- **Interfaces:** may display balances, claim states, and actions, but they cannot waive EVault contract checks.

EVault does **not** modify EON maximum supply, Guardian coherence rules, or EnergonController's deterministic progression.

## Topics for technical documentation

The contract-specific reference should cover:

1. Supported assets and decimals, using the exact production token addresses.
2. Commit and claim lifecycle, maturity and expiry.
3. Guardian-based eligibility and any activation conditions.
4. Reserve protections, liabilities, and payout-window budgets.
5. Fees, maturity tiers, and their on-chain calculation.
6. Custom errors, event definitions, and read-only monitoring methods.
7. Verified test cases and transaction references, separated from untested behavior.

These are documentation subjects, not claims that every configuration is active or that an audit has been completed.

## Source of truth

If there is a discrepancy between this overview, the EMP, the DApp, or the on-chain implementation, **the deployed contracts and live blockchain state control actual execution**.

For the umbrella architecture and other deployments, return to the [EnergonGrid overview](../README.md).

For the integration layer, see [Energon Network / EPA](network.md).
