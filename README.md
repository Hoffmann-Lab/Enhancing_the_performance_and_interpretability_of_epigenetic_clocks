# TFMethyl DNAm aging-clock

**Source code for the work "Enhancing the performance and interpretability of epigenetic clocks"**
🔗 [Preprint](https://www.biorxiv.org/content/10.1101/2025.10.07.680024v2)

---

## Overview

This repository contains the workflow, code, and model developed during the work. The project integrates both **R** and **Bash** code and provides **.Rmd** markdown for reproducible analysis.

---

## Repository Structure

| Script               |  Description                                                                                                                                        |
| -------------------- | -----------------------------------------------------------------------------------------------------------------------------------------------     |
|                                                                                                                                                                            |
| `/Run_TFMethyl`      | The newly developed epigenetic age prediction model for humans. Package contains trained model, script for execution, and a toy dataset in desired input format.                                                                                                                                                                      |
| `/helper_scripts`    | Scripts for creating TFBS whole genome annotations, performing footprinting analysis, and checking necessary R packages for `Analysis.Rmd`. More information available at `./helper_scripts/README`.                                                                                                                                                |
|                                                                                                                                                                            |
| `Analysis.Rmd`       | Source code for generating in-text figures and performing other necessary analyses for the study "Enhancing the performance and interpretability of epigenetic clocks".                                                                                                                                                                     |
| `Analysis.html`      | The knitted executed version of `Analysis.Rmd` for viewing in a web browser.                                                                        |
|                                                                                                                                                                            |

---

## 🧬 TFMethyl Usage

To run the TFMethyl clock, place a beta matrix file (named "beta_test_matrix.csv") at: `./Run_TFMethyl/` and run `source("./Run_TFMethyl/TFMethyl.R")` in an R environment. Detailed specifications for the input matrix, model, along with example test dataset are available at `./Run_TFMethyl/`.

## 🔧 Analysis Reproducibility

Analysis.Rmd is dependent on bunch of input data structures mounted at `./Data/` directory, and installed CRAN/Bioconductor packages. Before running the script, do as follows:

```bash
mkdir -p Data
cd Data/
wget link
```
Then first run `./helper_scripts/packages_check.R`, finally following the `Analysis.Rmd` in a R enviornment. 

## Notes

* The processed data (as`./Data`) required to run `Analysis.Rmd` is the ONLY missing directory (~16GBs) in this repository. 
* TFMethyl clock required data objects are included at (`./Run_TFMethyl/*.rds`). 

---
