# Quantitative Mosaic Generator (`system:quantitative-mosaic-generator`)

[简体中文](./README.md) | **English**

> **A Meta-Skill that generates first-principles mathematical Quantitative Mosaic investment research frameworks (Supply/Demand/Financial Model & Reverse-Engineering Scraping Nodes) to inject professionalism for any target stock (Ticker).**

## Overview

`quantitative-mosaic-generator` is a **Meta-Skill** built for AI coding and investment research agents (such as Google Antigravity, Claude Code, and OpenAI Codex).

When given any public company (`Ticker`) and its core business, this skill strictly prohibits vague qualitative clichés (such as "P/E relative valuation" or "strong industry tailwinds"). Instead, it forces the Agent to model the company from **first-principles physical units** (Watts, Test-Seconds, Wafers, Racks, Yield $\%$) and automatically generates a complete, reusable `SKILL.md` comprising:

1. **Physical & Commercial Ontology** (Base physical units and billing anchors)
2. **Supply & Demand Constraint Equations** ($Q_{\text{actual}} = \min(Q_{\text{supply}}, Q_{\text{demand}})$)
3. **Financial Translation & Operating Leverage Model** (Yield loss non-linearity, fixed depreciation absorption, and EPS elasticity)
4. **Reverse-Engineering High-Frequency Data Nodes** (Exact 8–10 digit Customs HS Codes, specific quarterly balance-sheet/cash-flow line items of upstream suppliers & downstream customers, and physical engineering trackers)
5. **Mandatory Quantitative Output Schema** (Parameter calibration table, binding bottleneck identification, and $\pm 5\%$ sensitivity shock matrix)

---

## Directory Structure

```text
quantitative-mosaic-generator/
├── SKILL.md                                       # Primary Meta-Skill instruction file (Zero-overhead progressive disclosure)
├── SKILL_EN.md                                    # English Meta-Skill specification (Lazy-loaded on demand, 0 idle context cost)
├── templates/
│   ├── target-company-mosaic-skill.md             # Standard Chinese output template for target companies
│   └── target-company-mosaic-skill-en.md          # Standard English output template for target companies
├── README.md                                      # Chinese documentation
├── README_EN.md                                   # English documentation
└── .gitignore                                     # Git ignore rules
```

---

## Installation

### 1. Google Antigravity
Clone directly into your global skills directory:
```bash
git clone https://github.com/akdunwu/quantitative-mosaic-generator.git ~/.gemini/config/skills/quantitative-mosaic-generator
```

### 2. OpenAI Codex / Claude Code
```bash
git clone https://github.com/akdunwu/quantitative-mosaic-generator.git ~/.codex/skills/quantitative-mosaic-generator
```

---

## Usage & Prompts

Simply prompt your agent in natural language (either in English or Chinese):
- `"Generate the Quantitative Mosaic Skill for [NVDA / NVIDIA] in English"`
- `"Generate the Quantitative Mosaic Skill for [Teradyne / TER]"`
- `"Use quantitative-mosaic-generator to build a physical supply-demand bottleneck model for [TSMC / TSM]"`
