# Reproducible Econometric Analysis Pipeline Using Cross-Country Data

## Project Overview

This project implements a **fully reproducible empirical analysis pipeline** for cross-country macroeconomic data, with a strong emphasis on **effective programming practices for applied economists**.

The goal is not to propose a novel economic theory, but to demonstrate how standard econometric workflows can be engineered as **modular, maintainable, testable, and reproducible software systems**, in line with best practices taught in the course *Effective Programming Practices for Economists*.

The pipeline programmatically acquires data, validates and cleans it, constructs features, estimates econometric models, and produces publication-ready outputs — all in a deterministic and reproducible manner.

---

## Data Source

The project uses **publicly available macroeconomic data** from the **World Bank Open Data API**.

Data are acquired programmatically (no manual downloads) to ensure reproducibility.

### Core Indicators

The analysis is based on the following World Bank indicators:

- **GDP per capita (constant USD)**
- **Inflation (CPI, annual %)**
- **Investment (% of GDP)**
- **School enrollment, secondary (%)**
- **Trade openness (% of GDP)**

To avoid unnecessary panel-data complexity while retaining economic relevance, the analysis focuses on a **cross-section of countries for a fixed year**.

---

## Models and Analysis

The pipeline estimates the following econometric models:

- **Ordinary Least Squares (OLS)**  
  - Continuous outcome: log GDP per capita  
  - Robust standard errors (HC-type)

- **Logit model**  
  - Binary outcome indicating high-inflation episodes

- **Probit model**  
  - Same binary outcome as in the Logit specification

Where appropriate, additional diagnostics and marginal effects are computed and reported.

The emphasis is on **clean model wrappers, consistent interfaces, and reproducible estimation**, rather than on implementing estimators from scratch.

---

## Outputs

Running the pipeline automatically produces:

- Cleaned and processed analysis datasets
- Summary statistics tables
- Regression tables (OLS, Logit, Probit) in **LaTeX format**
- Diagnostic and descriptive figures

All outputs are written to disk in a structured directory layout to support reproducible research workflows.

---

## Reproducibility

The project is fully reproducible:

- All dependencies are managed via **Pixi**
- The entire workflow can be executed via a small number of commands
- No manual data preparation steps are required
- Results are deterministic given the fixed configuration

Detailed instructions for setting up the environment and running the pipeline will be provided in the repository.

---

## Expected Contribution

This project demonstrates how **standard econometric analyses** commonly used in applied economics can be implemented as **robust, reproducible, and well-tested software systems**.

It illustrates effective programming practices that are directly relevant for empirical economists, including workflow decomposition, testing strategies, reproducibility, and research-oriented code organization.

