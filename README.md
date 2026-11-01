# Anthropic, PBC (Form S-1 / Ticker: ANT): Independent Feasibility & Valuation Audit

> A first-principles financial model and interactive stress-test evaluating Anthropic's October 26, 2026 Form S-1 registration statement, its $688.6B off-balance-sheet take-or-pay compute waterfall, and post-IPO valuation scenarios (2026-2030).

[![Python](https://img.shields.io/badge/Python-3.14%2B-blue.svg)](https://www.python.org/)
[![Tests: Pytest](https://img.shields.io/badge/Tests-19%20Passed-brightgreen.svg)]()

---

## Executive Summary

Anthropic's October 26, 2026 Form S-1 proves that frontier AI labs can generate tens of billions in commercial enterprise revenue ($16.29B in H1 2026; $11.56B in Q2 alone, or a $46.22B annualized run-rate), anchored by **Claude Code** and **~900% Net Revenue Retention (NRR)**.

However, stripping away GAAP accounting distortions reveals a critical capital-structure vulnerability at the proposed $1.5T-$2.0T IPO valuation:
1. **Two Opposite GAAP Mirages**:
   - The headline **-$80.75B H1 2026 GAAP net loss** is a non-cash artifact of marking $6.2B in Amazon convertible note principal up to $108.6B fair value (-$72.4B ASC 825-10 charge).
   - Conversely, the **85.4% accounting gross margin** ($2.38B Cost of Revenue on $16.29B revenue) is inflated because **$9.74B of R&D pre-training and research compute** is excluded from COGS. Because frontier model weights become obsolete in 9-15 months, pre-training is recurring maintenance COGS. Including total compute ($8.95B in H1 2026), **true compute-adjusted gross margin is 45.1%**.
2. **The $587.0B-$688.6B Take-or-Pay Compute Guillotine**:
   - As of June 30, 2026, Anthropic signed **$265.6B in fixed purchase commitments** + **$321.4B in uncommenced compute/data-center leases ($587.0B)**, expanding to **$688.6B** including Q3/October 2026 subsequent events across Google Cloud + TPUs ($252.0B), Broadcom/Apollo ($161.2B), SpaceX xAI ($120.5B), Amazon AWS ($110.0B), and Microsoft Azure ($44.9B).
   - By 2028, Anthropic's scheduled minimum compute outflow (~$86.0B/yr) absorbs **42.4% of the Big-4 hyperscalers' entire $202.9B/yr annual carrying cost**—shifting hardware depreciation risk onto Anthropic's $131.7B cash reserve.

---

## 2026-2030 Scenario Waterfall Summary

| Scenario (Probability) | 2028E Revenue | 2028E Compute Outflow | 2026-30 Deadweight Compute | 2029E Cash Reserve | 2028E Implied Market Cap | Return vs. $1.5T IPO | Solvency Verdict |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **1. Bull: Agentic Singularity (20%)** | $165.0B | $86.0B | $10.3B | **$300.2B** | **$2,610.2B** | **+74.0%** | `SOLVENT_SELF_FUNDING` |
| **2. Base: Rational Enterprise Plateau (50%)** | $85.0B | $77.4B | $115.6B | **$122.2B** | **$844.7B** | **-43.7%** | `SOLVENT_CASH_BUFFER_BURN` |
| **3. Bear: AI Bubble Burst / Deflation (30%)** | $40.0B | $64.5B | $182.9B | **$52.4B** | **$232.4B** | **-84.5%** | `SOLVENT_CASH_BUFFER_BURN` |
| **Probability-Weighted Expected Value** | $87.5B | $75.3B | $114.7B | **$136.9B** | **$1,014.1B** | **-32.4%** | Operational survivor; IPO overpriced |

---

## Quickstart & Interactive Dashboard

### 1. View the Interactive HTML Report
Open [`index.html`](./index.html) or [`docs/anthropic_s1_evaluation.html`](./docs/anthropic_s1_evaluation.html) in any browser:
```bash
open docs/anthropic_s1_evaluation.html
```

### 2. Run the Automated Test Suite
```bash
uv run --with pytest pytest repo/tests/ -v
```

### 3. Run the Python Simulation Engine
```bash
python3 repo/src/anthropic_s1_model.py
```
