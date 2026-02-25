# AUTONOME – MVP Prototype
## Deterministic Scoring & Emission Simulation

This folder contains the Minimal Viable Prototype (MVP) for AUTONOME – Competitive AI Fund Layer on Bittensor.

The MVP demonstrates the core mechanism of the subnet:

- Deterministic performance scoring
- Risk-adjusted evaluation
- Multi-miner comparison
- Emission weight mapping logic

This prototype validates the feasibility of the incentive design prior to full Bittensor testnet integration.

---

# MVP Objective

The objective of this MVP is to demonstrate:

1. How miner performance is evaluated deterministically
2. How multiple agents compete within the same evaluation window
3. How composite scores are computed
4. How emission weights can be derived from performance

This prototype simulates validator-side scoring logic.

---

# System Simulation Overview

In the full AUTONOME subnet:

- Users deposit capital into vault smart contracts
- Miners execute yield strategies
- Validators compute performance metrics from on-chain vault data
- Emissions are distributed based on weighted scores

In this MVP:

- Sample miner performance data is simulated
- Composite scoring is computed
- Emission allocation is derived proportionally

---

# Performance Metrics Used

Each miner is evaluated using four components:

1. ROI (Return on Investment)
2. Risk-Adjusted Return
3. Maximum Drawdown Control
4. Execution Consistency

Composite Score Formula:

Score =
(ROI × 0.40)
+ (Risk_Adjusted_Return × 0.30)
+ ((1 − Drawdown) × 0.20)
+ (Consistency × 0.10)

This ensures:

- High returns alone are insufficient
- Excessive volatility is penalized
- Large capital drawdowns reduce score
- Stable performance is rewarded

Yield without discipline is not intelligence.

---

# Emission Allocation Logic

After composite scores are computed:

Emission Weight = Miner Score / Sum of All Miner Scores

This ensures:

- Relative competition within each evaluation epoch
- Performance-based reward distribution
- No subjective intervention

Emission allocation is fully deterministic.

---

# Example Flow

1. Multiple miners submit strategy outputs.
2. Vault performance metrics are recorded.
3. Validator computes ROI, volatility proxy, drawdown, consistency.
4. Composite scores are calculated.
5. Scores are normalized.
6. Emission weights are assigned proportionally.

This logic directly maps to Bittensor weight assignment in Round 2.

---

# Why This MVP Matters

This MVP demonstrates that:

- The scoring framework is implementable
- Incentives can be computed deterministically
- Multi-agent competition is measurable
- Emission alignment with productivity is feasible

It validates the core economic logic of AUTONOME.

---

# Round 2 Integration Plan

The following components will be integrated in testnet deployment:

- Vault smart contracts for capital isolation
- Miner execution modules
- On-chain performance data retrieval
- Validator scoring integration with Bittensor metagraph
- Automated emission weight submission

The MVP scoring engine will directly connect to vault-derived data in Round 2.

---

# Design Philosophy

AUTONOME treats capital allocation as a measurable intelligence competition.

This prototype confirms:

- Scoring is objective
- Evaluation is reproducible
- Reward mapping is deterministic
- Collusion surface is minimized

Performance becomes the only path to reward.

---

# Summary

This MVP validates the core competitive logic of AUTONOME.

The next stage integrates this deterministic scoring model into a live Bittensor subnet with real vault execution.

AUTONOME  
Competitive AI Fund Layer on Bittensor
