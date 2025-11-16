### 0\. Understand what a Sort is.



A SORT takes all stock in the market and groups the on one or more characteristic.

sort by size | sort by book to market | sort by profitability | sort by investment | sort by past returns (momentum) | sort by accruals, beta. 



This is where our portfolio returns come from. our HML(value), RMW(profitability), CMA(investment). This is huge for our **2(d)** because this is where our variable creation comes from. 



### 1\. U.S. Research Returns Data



actual regression data, you can run the 3 or 5 factor model from here



### 2\. Univariate Sorts on Size, B/M, OP and Investment



this is not regression data, from now on the following sections are portfolios. in this section portfolios are created by sorting one variables at a time. 



Portfolios Formed on Size (ME)

\- Monthly value-weighted returns for portfolios sorted only on market equity (size).

\- Columns show different groupings: Lo 30 / Med 40 / Hi 30 (terciles), Lo 20 … Hi 20 (quintiles), Lo 10 … Hi 10 (deciles).

\- Smaller groups = smaller firms; larger groups = bigger firms.

\- Missing data are coded as -99.99 or -999.



Portfolios Formed on Book-to-Market (BE/ME)

\- Monthly value-weighted returns for portfolios sorted only on BE/ME.

\- BE/ME = book equity at the last fiscal-year-end of the prior calendar year divided by market equity at the prior December.

\- Same grouping structure: terciles, quintiles, deciles.



Portfolios Formed on Operating Profitability (OP)

\- Monthly value-weighted returns for portfolios sorted only on OP.

\- OP = operating profits (sales − COGS − SG\&A − interest expense) divided by book equity at the prior fiscal year end.

\- Same tercile/quintile/decile layout; extreme OP firms can make the highest/lowest deciles volatile.



Portfolios Formed on Investment (INV)

\- Monthly value-weighted returns for portfolios sorted only on INV (asset growth).

\- INV = (total assets at fiscal year t−1 − total assets at t−2) / total assets at t−2.

\- Same tercile/quintile/decile structure as the other univariate sorts.



### 3\. Bivariate Sorts on Size, B/M, Operating Profitability, Investment



This section shows portfolios based on two variables. 

Bivariate Sorts on Size × B/M, Size × OP, and Size × INV

\- These files contain monthly value-weighted returns for portfolios formed by sorting stocks on TWO characteristics at once: (1) Size (Small vs Big) and (2) either Book-to-Market (B/M), Operating Profitability (OP), or Investment (INV).



6 Portfolios Formed on Size × B/M (2×3)

\- Stocks are first split into Small and Big using NYSE median market equity.

\- Each Size group is then split into 3 B/M groups: LoBM (low B/M), BM2 (middle), HiBM (high B/M).

\- This produces 6 portfolios: SMALL LoBM, ME1 BM2, SMALL HiBM, BIG LoBM, ME2 BM2, BIG HiBM.

\- These 6 returns are the building blocks for the HML (value) factor and part of SMB.



6 Portfolios Formed on Size × OP (2×3)

\- Same structure as above, but the second variable is OP (Operating Profitability).

\- OP groups are: LoOP, OP2, HiOP.

\- Output portfolios: SMALL LoOP, SMALL HiOP, BIG LoOP, BIG HiOP, etc.

\- These are used to construct the RMW (profitability) factor.



6 Portfolios Formed on Size × Investment (2×3)

\- Same structure, but the second variable is INV (asset growth).

\- INV groups are: LoInv (conservative), Inv2, HiInv (aggressive).

\- These are used to construct the CMA (investment) factor.



25 Portfolios (5×5) and 100 Portfolios (10×10)

\- Same idea as 2×3, but finer grids (5×5 or 10×10).

\- Useful for research, robustness checks, or heatmaps of returns, but not required for constructing FF5 factors.



Interpretation of Columns (example from 6×B/M file):

\- SMALL LoBM: small-cap, low book-to-market (growth) stocks.

\- ME1 BM2: small-cap, neutral B/M.

\- SMALL HiBM: small-cap, high book-to-market (value).

\- BIG LoBM: large-cap, growth.

\- ME2 BM2: large-cap, middle B/M.

\- BIG HiBM: large-cap, value.

Monthly values represent the value-weighted return of each portfolio.



Overall Purpose:

\- These bivariate sorts are the core data used to build the Fama-French factors:

&nbsp; - SMB uses size spreads across these portfolios.

&nbsp; - HML uses high B/M minus low B/M across size groups.

&nbsp; - RMW uses high OP minus low OP.

&nbsp; - CMA uses low INV minus high INV.



### 4\. Three-Way Sorts on Size, B/M, OP, and INV



\- These files contain monthly value-weighted returns for 32 portfolios formed on three characteristics at once:

&nbsp; (1) Size (Small vs Big)

&nbsp; (2) A 4-way split of B/M, OP, or INV

&nbsp; (3) A second 4-way split of another variable.

\- Examples:

&nbsp; - Size × B/M × OP (2×4×4)

&nbsp; - Size × B/M × INV (2×4×4)

&nbsp; - Size × OP × INV (2×4×4)

\- Intended for advanced research on multidimensional anomalies; not used to build FF5 factors.



### 5\. Univariate Sorts on E/P, CF/P, and D/P



\- Portfolios sorted only on valuation ratios:

&nbsp; - E/P = earnings-to-price

&nbsp; - CF/P = cashflow-to-price

&nbsp; - D/P = dividend yield

\- Columns show terciles, quintiles, and deciles similar to other univariate sorts.

\- Useful for studying classic valuation anomalies.



### 6\. Bivariate Sorts on Size × E/P, Size × CF/P, and Size × D/P



\- Six portfolios formed by first splitting stocks into Small/Big, then into three valuation groups.

\- Examples: SMALL LoEP, SMALL HiEP, BIG LoEP, BIG HiEP.

\- Good for studying how valuation effects differ by size; not required for FF5.



### 7\. Sorts Involving Prior Returns



\- Momentum and reversal-based sorts.

\- Momentum Factor (Mom): long past 12–2 month winners, short losers.

\- Short-Term Reversal (ST Rev): 1-month reversal effect.

\- Long-Term Reversal (LT Rev): 3–5 year reversal effect.

\- Also includes:

&nbsp; - Size × Momentum (2×3, 5×5)

&nbsp; - Size × ST Rev (2×3, 5×5)

&nbsp; - Size × LT Rev (2×3, 5×5)

\- These are inputs to models like Carhart (4-factor) and reversal studies.



### 8\. Sorts Involving Accruals, Beta, Net Share Issues, Variance, Residual Variance



\- Univariate and bivariate portfolios built on additional anomaly characteristics:

&nbsp; - Accruals (balance sheet or cashflow)

&nbsp; - Market Beta (sorted portfolios)

&nbsp; - Net Share Issues (financing anomaly)

&nbsp; - Total Variance and Residual Variance (volatility anomalies)

\- Used for exploring alternative predictors; not part of FF5.



### 9\. Industry Portfolios



\- Standard industry return groups based on SIC classifications.

\- Offered in 5, 10, 12, 17, 30, 38, 48, and 49-industry versions.

\- Monthly and daily value-weighted returns.

\- Used in industry analysis, CAPM regressions, and portfolio construction; not used to build FF5.









