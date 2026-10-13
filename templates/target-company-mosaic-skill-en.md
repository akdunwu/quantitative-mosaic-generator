---
name: mosaic-<ticker-lowercase>
description: >-
  [<Company Name> (<Ticker>)] Quantitative Mosaic Investment Research Skill.
  Built on first-principles physical units (<base physical unit>), supply-demand bottleneck equations,
  operating leverage models, and reverse-engineering high-frequency data nodes.
---

# Quantitative Mosaic Model: <Company Name> (`<Ticker>`)

## Step 1: Physical & Commercial Ontology

* **Core Commercial Nature**: `<Capital Equipment / Consumables / Compute Infrastructure / Software / Energy>`
* **Base Physical Output Unit ($u_{\text{base}}$)**: `<e.g., 12-inch Equivalent Wafers / Test-Seconds / MWh / Racks>`
* **Monetization & Billing Physical Anchor**: `<e.g., Per System Acceptance / Per Test-Second Throughput / Per MW Leased>`

---

## Step 2: Supply & Demand Physical Equations ($Q_{\text{actual}} = \min(Q_{\text{supply}}, Q_{\text{demand}})$)

### 2.1 Supply Constraint Equation

$$Q_{\text{supply}}(t) = \min_{i \in \mathcal{B}} \left( \frac{C_i(t) \cdot \eta_i(t) \cdot Y_i(t)}{\alpha_i} \right)$$

| Symbol | Physical Definition | Physical Unit | Baseline Calibration | Constraint Mechanism |
| :--- | :--- | :--- | :--- | :--- |
| $C_1(t)$ | `<Bottleneck Component / Capacity Quota>` | `<Unit>` | `<Value Range>` | `<e.g., Sole-source supplier capacity>` |
| $\eta_1(t)$ | `<Effective Equipment Utilization>` | `%` | `<Value Range>` | `<e.g., Net of maintenance & changeover>` |
| $Y_1(t)$ | `<Composite Physical Yield>` | `%` | `<Value Range>` | `<e.g., First-pass packaging/test yield>` |
| $\alpha_1$ | `<Unit Physical Consumption Quota>` | `<Unit/Item>` | `<Value Range>` | `<e.g., Wafer area consumed per system>` |

### 2.2 Demand Driver Equation

$$Q_{\text{demand}}(t) = \sum_{k} \left( \frac{\text{CapEx}_k(t) \cdot \omega_k(t)}{P_{\text{sys}}(t)} \right) \cdot \gamma_{\text{attach}}(t) \cdot m_{\text{replace}}(t)$$

| Symbol | Physical Definition | Physical Unit | Baseline Calibration | Demand Driver Mechanism |
| :--- | :--- | :--- | :--- | :--- |
| $\text{CapEx}_k(t)$ | `<Downstream Customer CapEx>` | `USD / Local` | `<Value Range>` | `<Target customer capital budget>` |
| $\omega_k(t)$ | `<Target Node Value Share>` | `%` | `<Value Range>` | `<Share of CapEx flowing to this node>` |
| $\gamma_{\text{attach}}(t)$ | `<Physical Attach Multiplier>` | `<Units/Sys>` | `<Value Range>` | `<Intensity increase per generation>` |
| $m_{\text{replace}}(t)$ | `<Physical Replacement Coefficient>` | `1/Years` | `<Value Range>` | `<Inverse of physical wear/obsolescence cycle>` |

---

## Step 3: Financial Translation & Operating Leverage Model

### 3.1 Revenue & Gross Profit Equations
$$\text{Rev}(t) = Q_{\text{actual}}(t) \cdot \text{ASP}(t)$$
$$\text{COGS}(t) = \text{FC}_{\text{mfg}}(t) + Q_{\text{actual}}(t) \cdot \frac{v_{\text{raw}}(t)}{Y(t)}$$
$$\text{GP}(t) = \text{Rev}(t) - \text{COGS}(t)$$

### 3.2 Earnings Per Share (EPS) & Operating Leverage
$$\text{EPS}(t) = \frac{\big(\text{GP}(t) - \text{OpEx}_{\text{fixed}}(t) - \beta_{\text{var}} \cdot \text{Rev}(t) - I_{\text{net}}(t)\big) \cdot (1 - \tau_{\text{tax}})}{S_{\text{diluted}}(t)}$$

---

## Step 4: Reverse-Engineering High-Frequency Data Nodes

| Node Category | Exact Tracked Metric / Code | Data Source & Scraping Path | Mapped Variable | Lead Time |
| :--- | :--- | :--- | :--- | :--- |
| **Customs HS Code** | `HS Code: <8-10 Digit Code>` | `<Customs Trade Database / Port Data>` | $Q_{\text{supply}}, Q_{\text{actual}}$ | `<e.g., 1-2 Months>` |
| **Cross-Chain Filing Item** | `<Supplier/Customer + Exact Line Item>` | `<SEC EDGAR 10-Q / Local Filings>` | $C_1(t), \text{CapEx}_k(t)$ | `<e.g., 1 Quarter>` |
| **Physical High-Freq Node** | `<Grid Queue MW / Air Cargo / FSE Jobs>` | `<Specific Registry or Industry Portal>` | $\eta(t), Q_{\text{demand}}(t)$ | `<e.g., Weekly / Real-time>` |

---

## Step 5: Mandatory Output Schema

When invoking this Skill to analyze `<Ticker>`, the Agent must output:
1. **Core Physical Parameter Table**: Real-time extracted values and sources for all physical parameters in the current period.
2. **Bottleneck Verdict**: Explicit calculation of $Q_{\text{supply}}$ vs. $Q_{\text{demand}}$, identifying the single binding constraint determining $Q_{\text{actual}}$.
3. **Sensitivity Shock Matrix**: Quantified elasticity impact on $\text{Rev}$, $\text{GM}\%$, and $\text{EPS}$ when the binding bottleneck variable or yield $Y$ fluctuates by $\pm 5\%$.
