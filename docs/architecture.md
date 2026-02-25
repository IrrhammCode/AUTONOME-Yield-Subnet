# Architecture

## Overview

AUTONOME – Yield Subnet is designed as a competitive AI capital allocation network operating on Bittensor.

The subnet transforms DeFi yield optimization into a measurable intelligence competition between AI agents (miners), validated by objective on-chain metrics computed by validators.

The architecture enforces:

- Non-custodial capital handling
- On-chain verifiability
- Deterministic performance evaluation
- Economic alignment between participants

---

## System Components

### 1. Vault Smart Contracts

Vault contracts serve as controlled execution environments for strategy deployment.

Responsibilities:
- Accept user deposits (stablecoins)
- Restrict miner execution permissions
- Record all capital flows on-chain
- Provide transparent accounting data
- Enforce execution boundaries

Miners never directly custody user funds.
All strategy execution occurs through vault logic.

---

### 2. Miners (AI Yield Agents)

Miners are AI-driven strategy engines.

Responsibilities:
- Stake Alpha tokens to participate
- Submit strategy logic
- Execute yield allocation strategies via vault contracts
- Optimize capital across DeFi protocols
- Manage rebalancing and risk

Each miner operates independently and competes within a defined performance window.

Performance is evaluated purely on measurable output.

---

### 3. Validators (Performance Auditors)

Validators are responsible for scoring miner performance.

Responsibilities:
- Retrieve vault performance data
- Compute financial performance metrics
- Normalize scores across miners
- Assign weight within the Bittensor metagraph

Validators do not evaluate strategy design.
They evaluate measurable outcomes only.

---

## Operational Flow

### Step 1 – Capital Deposit

Users deposit stablecoins into subnet vault contracts.

Funds are programmatically allocated to miner-controlled execution modules.

---

### Step 2 – Strategy Commitment

Miners:
- Stake Alpha tokens
- Commit strategy configuration
- Lock parameters for evaluation period

This prevents mid-cycle manipulation.

---

### Step 3 – Execution Window

During a predefined epoch:

- Miner executes yield strategies
- All transactions remain on-chain
- Capital allocation decisions are recorded

Execution window length is configurable (e.g., 7–30 days).

---

### Step 4 – Performance Measurement

At the end of the evaluation window, validators compute:

- Net ROI
- Volatility proxy
- Maximum drawdown
- Capital efficiency ratio
- Execution consistency

All metrics derive from vault transaction history.

---

### Step 5 – Score Calculation

Validators compute performance score:

Score =
(ROI_normalized × w1)
+ (Risk_adjusted_return × w2)
+ (Drawdown_penalty × w3)
+ (Consistency × w4)

Weights are governance-configurable.

Scores are submitted to the Bittensor network.

---

### Step 6 – Reward Distribution

Based on validator-assigned weights:

- TAO emissions are distributed
- Performance fees are allocated
- Reputation metrics update

---

## Capital Isolation Model

To prevent misuse:

- Vault contracts enforce allocation boundaries
- Strategy execution functions are restricted
- Risk thresholds can be enforced at contract level
- Withdrawal functions remain user-controlled

Capital never enters miner-controlled wallets.

---

## Reputation Layer

Each miner maintains:

- Historical ROI performance
- Risk profile history
- Stake-weight ratio
- Slashing history

Reputation influences future allocation weight.

---

## Validator Integrity Layer

Validators are economically aligned through:

- Staked participation
- Emission dependency on scoring accuracy
- Slashing for deviation patterns
- Cross-validator consistency checks

Validators are incentivized toward objective computation.

---

## Scalability Considerations

The architecture supports:

- Multiple vault instances
- Strategy category segmentation
- Cross-chain execution modules
- Progressive decentralization of capital allocation

Yield optimization is the initial deployment vertical.

The architecture is extensible toward broader capital coordination use cases.

---

## Security Principles

- Non-custodial capital management
- Deterministic evaluation logic
- On-chain transparency
- Economic disincentives for manipulation
- Stake-based participation gating

---

## Design Philosophy

AUTONOME treats capital allocation as an intelligence competition.

Performance is:

- Observable
- Quantifiable
- Economically valuable

This aligns naturally with Bittensor’s reward model.