---
name: quantitative-mosaic-generator
description: >-
  Meta-Skill for generating a mathematical Quantitative Mosaic investment research framework
  (Supply/Demand/Financial Model & Reverse-Engineering Scraping Nodes) for any target company (Ticker).
---

# Meta-Skill: Quantitative Mosaic Generator (`system:quantitative-mosaic-generator`)

## Objective & Purpose
When the user inputs any target company (Ticker) and its core business, the system must automatically generate a rigorous investment research configuration file (`SKILL.md`) containing **exact mathematical equations**, **physical variable constraints**, and **reverse-engineered high-frequency data nodes**.

> **Core Iron Law**: Strictly prohibit empty qualitative clichés such as "relative P/E valuation," "high industry prosperity," or "deep moat." Every derivation must be anchored to **first-principles physical units** (e.g., Watts $\text{W}$, Test-Seconds $\text{s}$, Physical Units $\text{Units}$, Wafers $\text{Wafers}$, Racks $\text{Racks}$, Composite Yield $Y\%$).

---

## Framework Generation Rules

When generating a dedicated Quantitative Mosaic `SKILL.md` for a target company, strictly execute the following 5 steps:

### Step 1: Define Physical & Commercial Ontology
1. **Supply-Chain Physical Nature**: Identify the physical category of the company's core product within the value chain (Capital Equipment / Consumables / Compute Infrastructure / Industrial Software License / Energy Medium).
2. **Base Physical Dimension ($u_{\text{base}}$)**: Define the most fundamental physical unit of output and its time dimension (e.g., $\text{GPU-Hours}$, ATE $\text{Test-Seconds}$, 12-inch equivalent $\text{Wafers/Month}$, Liquid-Cooled $\text{Racks/Quarter}$, Effective $\text{MW}$).
3. **Monetization Anchor**: Specify the exact physical consumption mechanism tied to customer billing (per throughput volume, per installed base, per operating hour, or yield-sharing).

---

### Step 2: Construct Supply & Demand Equations ($Q_{\text{actual}} = \min(Q_{\text{supply}}, Q_{\text{demand}})$)

#### 1. Supply Constraint Equation
Formulate an explicit mathematical equation identifying the critical upstream components, cleanroom space, tool lead times, or physical bottlenecks constraining effective output (e.g., transformer capacity/power quota, sole-source supplier allocation, yield ramp curve):

$$Q_{\text{supply}}(t) = \min_{i \in \mathcal{B}} \left( \frac{C_i(t) \cdot \eta_i(t) \cdot Y_i(t)}{\alpha_i} \right)$$

* **$C_i(t)$**: Nominal physical quota or rated capacity of bottleneck resource $i$ in period $t$ (e.g., CoWoS wafer allocation, chamber deliveries, substation approved MW).
* **$\eta_i(t)$**: Equipment utilization rate or effective uptime ratio ($\in [0, 1]$).
* **$Y_i(t)$**: Composite physical yield rate ($\in [0, 1]$).
* **$\alpha_i$**: Unit consumption coefficient of upstream physical resource $i$ per unit of final product.
* **Requirement**: Explicitly define the mathematical symbol, physical unit, current baseline range, and physical meaning for every variable.

#### 2. Demand Driver Equation
**Strictly prohibit using macro GDP or broad industry CAGR.** Demand must be decomposed as a **function of downstream CapEx** or a **physical replacement multiplier** (e.g., Penetration Rate $\times$ Installed Base Replacement Cycle $\times$ Physical Intensity Multiplier):

$$Q_{\text{demand}}(t) = \sum_{k \in \mathcal{C}} \left( \frac{\text{CapEx}_k(t) \cdot \omega_k(t)}{P_{\text{system}, k}(t)} \right) \cdot \gamma_{\text{attach}}(t) \cdot m_{\text{replace}}(t)$$

Or driven by physical throughput time:

$$Q_{\text{demand}}(t) = N_{\text{installed}}(t) \cdot \rho_{\text{penetration}}(t) \cdot \frac{\tau_{\text{unit}}(t)}{T_{\text{cycle}}}$$

* **$\text{CapEx}_k(t)$**: Domain-specific capital expenditure of downstream core customer $k$ in period $t$.
* **$\omega_k(t)$**: Share of CapEx allocated to the target physical node.
* **$\gamma_{\text{attach}}(t)$**: Physical attach rate or channel multiplier per system.
* **$\tau_{\text{unit}}(t)$**: Physical processing time or consumption quota per unit/die (e.g., ATE test seconds per chip).

#### 3. Actual Shipment / Settlement Volume
$$Q_{\text{actual}}(t) = \min\Big(Q_{\text{supply}}(t),\; Q_{\text{demand}}(t)\Big)$$

---

### Step 3: Build Financial Translation Model

Establish a closed-loop analytical model translating physical shipments ($Q_{\text{actual}}$) and Average Selling Price ($\text{ASP}$) into Revenue ($\text{Rev}$), Gross Profit ($\text{GP}$), Operating Income ($\text{EBIT}$), and Earnings Per Share ($\text{EPS}$), explicitly capturing fixed-cost absorption and operating leverage:

1. **Revenue Equation**:
   $$\text{Rev}(t) = \sum_{j} Q_{\text{actual}, j}(t) \cdot \text{ASP}_j(t)$$
   Where $\text{ASP}_j(t) = \text{ASP}_{j,0} \cdot (1 + \Delta_{\text{mix}}(t)) \cdot (1 - \delta_{\text{erosion}}(t))$, isolating product mix upgrades from annual price erosion.

2. **COGS & Gross Profit Equation**:
   $$\text{COGS}(t) = \text{FC}_{\text{mfg}}(t) + \sum_{j} Q_{\text{actual}, j}(t) \cdot \frac{v_{\text{raw}, j}(t)}{Y_j(t)}$$
   $$\text{GP}(t) = \text{Rev}(t) - \text{COGS}(t), \quad \text{GM}\%(t) = 1 - \frac{\text{FC}_{\text{mfg}}(t)}{\text{Rev}(t)} - \frac{\overline{v_{\text{raw}}}(t)}{\overline{Y}(t) \cdot \overline{\text{ASP}}(t)}$$
   * **$\text{FC}_{\text{mfg}}(t)$**: Fixed manufacturing depreciation and rigid labor amortization.
   * **$v_{\text{raw}, j}(t)$**: Pre-yield unit variable raw material and energy cost; dividing by yield $Y_j(t)$ captures the non-linear margin impact of yield fluctuations.

3. **EPS Equation**:
   $$\text{EPS}(t) = \frac{\big(\text{GP}(t) - \text{OpEx}_{\text{fixed}}(t) - \beta_{\text{var}} \cdot \text{Rev}(t) - I_{\text{net}}(t)\big) \cdot (1 - \tau_{\text{tax}})}{S_{\text{diluted}}(t)}$$

4. **Degree of Operating Leverage (DOL)**:
   $$\frac{\partial \ln(\text{EPS})}{\partial \ln(Q_{\text{actual}})} = \frac{Q_{\text{actual}} \cdot \big(\text{ASP} - v_{\text{raw}}/Y - \beta_{\text{var}}\cdot \text{ASP}\big)}{\text{GP} - \text{OpEx}_{\text{fixed}} - \beta_{\text{var}} \cdot \text{Rev} - I_{\text{net}}}$$

---

### Step 4: Define Reverse-Engineering Data Nodes

* **No vague advice** (e.g., "check financial reports" or "monitor industry news").
* **Must specify scrapeable, verifiable indicator-level nodes**:
  1. **Customs & Physical Trade Tracking**: Exact 6-to-10 digit **HS Codes (Harmonized System)**, specific port/state/province origin codes, and physical units (kg / units) to back-solve physical shipment tonnage or volume.
  2. **Cross-Chain Financial Line Items**: Specific quarterly filing line items of sole-source suppliers or key customers (e.g., "Contract Liabilities", "Purchase Commitments", "Construction in Progress (CIP) transfers", "Raw Materials vs. WIP Inventory split").
  3. **High-Frequency Physical & Engineering Alternative Data**: Air cargo tonnage indices (e.g., Taoyuan/Incheon electronics air freight), regional grid interconnection queues (ISO Queue MW), specialty gas consumption, job postings for specific engineering roles (e.g., Field Service Engineers / FSE headcount), or fab tool move-in tender filings.

---

### Step 5: Mandatory Output Schema

Require any Agent executing the generated company Skill to output:
1. **Core Physical Parameter Table**: Current calibrated values, physical units, data sources, and confidence levels for all supply and demand variables.
2. **Bottleneck Identification**: Quantitative comparison of $Q_{\text{supply}}(t)$ vs. $Q_{\text{demand}}(t)$ to determine whether the company is currently supply-constrained or demand-constrained, pinpointing the exact binding variable.
3. **Financial Forecast & Sensitivity Matrix**: Quantify the absolute and percentage impact on $\text{Rev}$, $\text{GM}\%$, and $\text{EPS}$ when key physical variables (e.g., yield $Y$, bottleneck quota $C_i$, processing time $\tau$, $\text{ASP}$) shift by $\pm 5\%$.

---

## Execution Protocol

If the user says: "Generate the Quantitative Mosaic Skill for `[Company X]`" (or requests it in English), strictly follow the architecture of this document and `./templates/target-company-mosaic-skill-en.md` to output a complete Markdown specification with LaTeX mathematical formulas and exact data nodes.
