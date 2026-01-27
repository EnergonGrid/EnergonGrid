# ENERGON

ENERGON is a deterministic, state-driven protocol live on Flare Mainnet.

It is designed to persist without optimization, incentives, or discretionary governance.

---

## Overview

ENERGON replaces yield-driven mechanics with immutable progression rules derived entirely from on-chain state.

The protocol introduces:
- **EON** — a finite energy unit (ERC-20)
- **EnergonCube** — a capped identity primitive (ERC-721)
- **EnergonController** — a state computation and enforcement layer

All protocol behavior is observable, auditable, and non-reactive.

ENERGON does not promise returns.  
It does not adapt to markets.  
It exists as a long-lived protocol artifact.

---

## Design Principles

ENERGON is built on the following principles:

- State over strategy  
- Observation over optimization  
- Determinism over discretion  
- Finality over governance flexibility  
- Persistence over growth  

The protocol intentionally avoids:
- Yield incentives
- Farming mechanics
- Off-chain schedulers
- Cron jobs
- Third-party automation
- Governance-controlled monetary policy

All meaningful behavior is anchored to on-chain, verifiable state.

---

## Protocol Architecture

ENERGON consists of a minimal, immutable contract stack:

- **EnergonToken (EON)**  
  ERC-20 utility token with a hard-capped supply of 30,000,000 EON, deterministic emissions, fixed halving schedule, and genesis-bounded burn logic.

- **EnergonCube**  
  ERC-721 identity NFT with a maximum supply of 1,000,000 units and a strict one-cube-per-wallet constraint.

- **EnergonController**  
  Computes global protocol state (Energon Height), enforces progression eligibility, and regulates cooldowns.  
  The controller executes no automated actions and relies solely on explicit interaction and on-chain reads.

---

## Genesis & Time Anchoring

ENERGON defines genesis exclusively by on-chain contract deployment.

**Protocol Genesis:**  
December 20, 2025 · 23:07 (UTC)

This timestamp is immutable and serves as the sole reference for:
- emissions
- halving epochs
- burn duration
- terminal supply conditions

UI launches or ecosystem milestones do not affect protocol time.

---

## Identity Model

ENERGON enforces a permanent identity constraint:

**One Wallet · One Cube · One Guardian**

Cubes do not generate yield, confer governance rights, or provide upgrade paths.  
They establish identity, not control.

State interpretation:
- 0 cubes → no participation
- 1 cube → coherent state
- 2+ cubes → fractured state

This is not a recommendation or preference.  
It is an enforced condition.

---

## Governance

ENERGON minimizes governance by design.

Governance cannot modify:
- token supply
- halving schedules
- burn parameters
- genesis timestamp
- emission termination conditions
- Energon Height computation

Permitted governance scope is limited to documentation and interface evolution.  
Protocol math is final.

---

## Closing

ENERGON is intentionally finite.

By fixing identity, energy, time, and decay, the protocol becomes predictable, auditable, non-reactive, and long-lived.

The protocol does not interpret intent.  
It reads state.

Observation precedes action.

Minimal surface. Observable state. ENERGON.
