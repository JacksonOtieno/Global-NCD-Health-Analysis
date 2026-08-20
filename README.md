# Global NCD Health Analysis

## Project Overview

Analysis of global noncommunicable disease (NCD) mortality trends across all WHO-tracked countries (2000-present), examining how NCD burden has changed over time and whether different mortality measures move together.

**Core question:** How has the global probability of dying prematurely (age 30-70) from the four major NCDs (cardiovascular disease, cancer, diabetes, chronic respiratory disease) changed over time, and how does it relate to the age-standardized NCD mortality rate across countries?

## Data Source

- **Source:** WHO Global Health Observatory (GHO) OData API
- **Indicators:**
  - `NCDMORT3070` — Probability (%) of dying between age 30-70 from the four major NCDs (SDG 3.4.1)
  - `WHS2_131` — Age-standardized NCD mortality rate (per 100,000 population)
- **Coverage:** All WHO member countries, annual data
- **Access date:** August 2026

## Tools

- **Python** (Google Colab) — data acquisition, initial cleaning
- **R** — exploratory analysis and statistical work *(planned)*
- **Power BI** — dashboard *(planned)*

## Project Status

- [x] Data pulled from GHO API (both indicators, ~12,900 rows each)
- [ ] Data cleaning (filtering to country-level rows, resolving sex-disaggregation, handling data-quality flags)
- [ ] Exploratory analysis
- [ ] Dashboard
- [ ] Write-up

## Repository Structure

## Notes on Data Quality

The raw GHO pull includes rows beyond country level (`REGION`, `WORLDBANKINCOMEGROUP`, `GLOBAL` aggregates) which will be filtered out during cleaning. Some country-years carry a WHO methodology caveat flagged in the `Comments` field — this will be documented rather than silently dropped.
