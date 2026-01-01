# FFM — Empirical Replication & Robustness Analysis

This repository contains an academic replication of a published empirical study.  
The objective is to reproduce the main empirical results, evaluate the transparency of the original methodology, and assess robustness to alternative specifications.

The project is strictly replicative and methodological in nature.

## Environment & Requirements

The analysis is implemented in Python using Jupyter Notebooks.

- Python ≥ 3.8  
- Jupyter Notebook or JupyterLab  
- Required packages:
  - pandas
  - numpy
  - statsmodels
  - scikit-learn
  - matplotlib
  - seaborn

Install dependencies:

pip install pandas numpy statsmodels scikit-learn matplotlib seaborn
Using a virtual environment is recommended for reproducibility.

## Reproducing the Results

1. Clone the repository:

git clone https://github.com/ignaciomacan/FFM.git
cd FFM

2. Launch Jupyter:

jupyter notebook

3. Run notebooks in order:
- `FFM_DRAFT_11.20.ipynb`: core replication of the original results  
- `section3work.ipynb`: robustness checks and alternative specifications  

Ensure all file paths correctly reference the `data/` directory.

## Outputs

- `resultsSOP.csv`: consolidated numerical replication results  
- `josh_tables/`: formatted tables for reporting or LaTeX integration  
- `table9.png`: static figure illustrating a key replicated result

## Methodological Notes

The replication prioritizes exact reconstruction of the original regressions, explicit documentation of data transformations, and systematic sensitivity analysis. Any undocumented implementation choices or deviations are noted directly in the notebooks.

## Limitations

Some methodological decisions in the original study are not fully documented. Minor numerical discrepancies may arise due to software versions, rounding conventions, or data handling assumptions. Results should be interpreted strictly as a replication exercise.

## Citation

If referencing this repository:

Macan, Ignacio (2025).  
FFM: Empirical Replication and Robustness Analysis.  
GitHub repository: https://github.com/ignaciomacan/FFM

## Contact

Use GitHub Issues for questions, corrections, or replication feedback.
