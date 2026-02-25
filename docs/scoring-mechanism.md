# Scoring Mechanism

## Design Objective

The scoring mechanism converts on-chain capital performance into a deterministic performance score.

The system must:

- Reward sustainable yield
- Penalize excessive risk
- Penalize large drawdowns
- Reward execution stability
- Prevent short-term exploit behavior

All metrics are derived from verifiable vault transaction data.

No subjective judgment is involved.

---

## Evaluation Window

Performance is measured within a fixed evaluation epoch.

Example:
- 7 days
- 14 days
- 30 days

Miners commit to strategy parameters for the duration of the window.

Scores are computed at epoch conclusion.

---

## Core Performance Metrics

### 1. Net Return (ROI)

ROI = (Ending Capital − Starting Capital) / Starting Capital

This measures absolute performance.

However, ROI alone is insufficient.

---

### 2. Risk-Adjusted Return

We define a simplified Sharpe-like metric:

Risk_Adjusted_Return = ROI / Volatility

Where volatility is derived from:

- Standard deviation of periodic returns
- Or variance proxy based on daily net change

This prevents high-risk strategies from dominating.

---

### 3. Maximum Drawdown

Max_Drawdown = Maximum observed peak-to-trough decline during evaluation window.

Large drawdowns indicate poor capital protection.

Penalty factor:

Drawdown_Penalty = 1 − Max_Drawdown

Higher drawdown reduces final score.

---

### 4. Execution Consistency

Consistency measures stability of returns across sub-periods.

Example:

Consistency = 1 − Variance_of_Daily_Returns

This penalizes erratic or single-event-driven performance.

---

## Normalization

To prevent score distortion:

Each metric is normalized across participating miners within the same epoch.

For metric M:

Normalized_Miner_Value =
(Miner_Value − Min_Value) / (Max_Value − Min_Value)

Normalization ensures:

- Fair comparison
- Relative competition
- Resistance to extreme outliers

---

## Composite Score Formula

Final Score:

Score =
(w1 × ROI_normalized)
+ (w2 × Risk_Adjusted_normalized)
+ (w3 × Drawdown_Penalty_normalized)
+ (w4 × Consistency_normalized)

Example default weights:

w1 = 0.40  
w2 = 0.30  
w3 = 0.20  
w4 = 0.10  

Weights are governance-configurable.

---

## Safeguards Against Score Manipulation

### 1. Capital Scaling Neutrality

ROI is percentage-based.
Large capital does not guarantee higher score.

---

### 2. Flash Strategy Protection

Strategies that produce extreme short-term spikes but collapse later are penalized by:

- Drawdown factor
- Consistency metric

---

### 3. Over-Leverage Protection

Excessive leverage increases volatility, reducing risk-adjusted return.

The scoring system naturally disincentivizes unstable leverage.

---

### 4. Minimum Activity Threshold

Miners must execute a minimum number of transactions or capital movements.

Inactive capital farming yields low score.

---

## Score to Emission Conversion

Validator-submitted scores are converted into weights within the Bittensor metagraph.

Emission Allocation ∝ Score × Validator Weight

Higher score directly increases emission share.

---

## Reputation Update

After each epoch:

- Historical performance stored
- Long-term moving average computed
- Reputation index updated

Reputation influences:

- Future capital allocation
- Visibility ranking
- Governance weight

---

## Statistical Stability Considerations

To prevent oscillation:

- Exponential moving averages may be applied
- Extreme outliers capped
- Minimum participation thresholds enforced

These measures ensure:

- Predictable competition
- Stable incentive alignment
- Reduced gaming surface

---

## Summary

The scoring mechanism:

- Rewards measurable performance
- Penalizes instability
- Discourages reckless risk
- Ensures deterministic validator computation
- Aligns emissions with economic productivity

Capital intelligence becomes quantifiable.

And quantifiable intelligence becomes rewardable.