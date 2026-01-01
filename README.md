# FFM — Fama-French Five-Factor Model Replication

This repository contains a full empirical replication of the **Fama–French Five-Factor Asset Pricing Model**.  
The project was completed as a final replication and critical analysis assignment for **Economics 430 (UCLA)**, with the objective of reproducing the original results, assessing model implementation choices, and evaluating empirical robustness.

The Fama–French Five-Factor Model is a cornerstone of modern empirical finance and asset pricing, making this replication directly relevant for research, quantitative finance, and data-driven economic analysis.

## Why This Project Matters

The Fama–French Five-Factor Model is widely used in:
- empirical asset pricing research
- portfolio evaluation and risk attribution
- quantitative finance and investment analysis
- academic and industry-facing econometric work

This project demonstrates:
- the ability to replicate a canonical empirical model from the literature
- proficiency with real-world financial datasets
- disciplined econometric workflow (data cleaning, estimation, diagnostics, robustness)
- critical evaluation of published empirical results

These skills are directly applicable to research assistant roles, quantitative analyst positions, and data-focused economics or finance roles.

## How to Navigate This Repository

The repository is organized to mirror a standard academic replication workflow.  
Each folder and file corresponds to a specific stage of the replication process.

FFM/
├── data/                     # Raw and processed factor/portfolio datasets
├── original_paper/           # Fama-French paper and reference materials
├── project_instructions/     # Assignment description and grading criteria
├── FFM_DRAFT_11.20.ipynb     # Main replication notebook
├── section3work.ipynb        # Robustness checks and additional analysis
├── resultsSOP.csv            # Consolidated replication results
├── josh_tables/              # Exported regression tables (report / LaTeX-ready)
├── table9.png                # Static figure reproducing a key table/result
└── README.md

## Folder and File Descriptions

**data/**  
Contains all raw and processed datasets used in the replication, including factor returns and portfolio-level data. Any data cleaning and transformations used for estimation originate from this directory.

**original_paper/**  
Holds the original Fama–French Five-Factor Model paper and supporting reference material used to guide replication decisions.

**project_instructions/**  
Contains the original assignment prompt and grading rubric, outlining replication requirements, robustness checks, and evaluation criteria :contentReference[oaicite:0]{index=0}.

**FFM_DRAFT_11.20.ipynb**  
Primary replication notebook. Implements the core five-factor regressions, reproduces key tables, and documents methodological choices.

**section3work.ipynb**  
Focused notebook for robustness checks, alternative specifications, and diagnostic analysis beyond the baseline model.

**resultsSOP.csv**  
Structured output of the main regression results for easy comparison, reporting, or downstream analysis.

**josh_tables/**  
Contains formatted regression tables suitable for inclusion in written reports or LaTeX documents.

**table9.png**  
Static visualization reproducing a key result from the original paper.


## Replicated Model

This project replicates the **Fama–French Five-Factor Model**, which extends the traditional three-factor model by incorporating:
- market excess returns
- size (SMB)
- value (HML)
- profitability (RMW)
- investment (CMA)

The replication evaluates whether these factors jointly explain cross-sectional variation in asset returns, consistent with the original findings.


## Notes on Interpretation

This repository is intended as:
- an academic replication exercise
- a demonstration of applied econometric and financial modeling skills
- a transparent, reproducible reference for professional review

Results should be interpreted as a replication and methodological assessment, not as a modification or extension of the original Fama–French framework.


