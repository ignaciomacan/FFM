# Replication of "A Five-Factor Asset Pricing Model" (Fama & French, 2015)

**Econ 430 — Empirical Project 2**

---

## What This Project Does

This project replicates the empirical analysis from:

> Fama, Eugene F., and Kenneth R. French. "A Five-Factor Asset Pricing Model." *Journal of Financial Economics* 116 (2015): 1–22.

The original paper proposes a five-factor model to explain cross-sectional variation in stock returns. We replicate their OLS time-series regressions and GRS joint tests using publicly available data from the Kenneth R. French Data Library.

---

## Research Question

Does a five-factor model (Market, Size, Value, Profitability, Investment) better explain average portfolio returns than the three-factor model? Specifically:

- Are RMW (Profitability) and CMA (Investment) statistically significant after controlling for the other three factors?
- Does the five-factor model reduce unexplained alphas relative to the three-factor model?
- Is the model rejected by the Gibbons-Ross-Shanken (GRS) joint test?

---

## Data

All data come from the [Kenneth R. French Data Library](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html).

| File | Description |
|------|-------------|
| `data/five_factor_model/factors/5f_data.csv` | Five-factor monthly returns (MKT-RF, SMB, HML, RMW, CMA, RF) |
| `data/three_factor_model/factors/3f_data.csv` | Three-factor monthly returns |
| `data/five_factor_model/portfolios/` | Six sets of test portfolios (25 and 32 portfolio sorts) |
| `data/three_factor_model/portfolios/` | 25 Size × B/M portfolios (for three-factor baseline) |

**Sample period:** July 1963 – December 2013 (606 months) for the five-factor model, matching the original paper. The three-factor baseline uses the full available history through December 2013.

---

## Method

For each test portfolio, we estimate:

$$R_{it} - R_{ft} = \alpha_i + \beta_{MKT}(R_{Mt} - R_{ft}) + \beta_{SMB}\,SMB_t + \beta_{HML}\,HML_t + \beta_{RMW}\,RMW_t + \beta_{CMA}\,CMA_t + \varepsilon_{it}$$

- OLS time-series regression with HAC standard errors (Newey-West, 12 lags)
- Six test portfolio sets: 25 Size×BM, 25 Size×INV, 25 Size×OP, 32 ME×BM×INV, 32 ME×BM×OP, 32 ME×OP×INV
- GRS (1989) joint test of $H_0: \alpha_1 = \alpha_2 = \cdots = \alpha_N = 0$

---

## Key Results

- Factor summary statistics closely match the original paper (e.g., MKT mean = 0.50%, SMB = 0.28%)
- HML–CMA correlation of 0.70 matches exactly, supporting the paper's argument that HML is largely redundant
- Five-factor model reduces the small-growth alpha from −0.74% (t = −4.78) to −0.28% (t = −3.25)
- GRS tests reject the model at p < 0.01 across all portfolio sets
- **Replication is partial**: qualitative patterns and coefficient signs match; exact magnitudes differ, primarily due to the use of HML rather than the orthogonalized HML° used in the published tables, and HAC vs. standard OLS standard errors

---

## Repository Structure

```
fama_french_replication.ipynb   Main analysis notebook (run top to bottom)
data/
  five_factor_model/
    factors/5f_data.csv         Five-factor monthly returns
    portfolios/                 Six test portfolio CSV files
  three_factor_model/
    factors/3f_data.csv         Three-factor monthly returns
    portfolios/                 25 Size×BM portfolios
paper/
  FFM.pdf                       Original Fama & French (2015) paper
  table9.png                    Reference table from the paper (used in notebook)
outputs/
  ff_stats.csv                  Summary statistics table (saved from prior run)
  grs_df.csv                    GRS test results (saved from prior run)
  resultsSOP.csv                Size×OP regression results (saved from prior run)
```

---

## How to Run

```bash
# Install dependencies
pip install -r requirements.txt

# Open the notebook
jupyter notebook fama_french_replication.ipynb
```

Run all cells from top to bottom. The **setup cell at the beginning of Section 3** loads all data and runs all regressions; every subsequent cell in that section depends on it. Estimated runtime: 3–5 minutes (seven sets of 25–32 portfolio regressions each with HAC standard errors).

---

## Dependencies

See `requirements.txt`. Main packages:

- Python 3.9+
- pandas, numpy
- statsmodels (OLS, HAC standard errors)
- scipy (GRS test F-distribution)
- matplotlib, seaborn
