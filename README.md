# Benford First-Digit Analysis of Provincial Vote Totals

**Author:** Cameron Batts

## Problem
Compare the first digits of 30 reported provincial vote totals with an explicit Benford reference distribution.

## Approach
Parse comma-separated vote totals as numeric, validate positive integer counts and compare all nine first-digit frequencies with log10(1+1/d). Retain the chi-square approximation and add a proposed fixed-null Monte Carlo calculation for small expected counts.

## Verified findings
Independent Python calculation reproduced first-digit counts [5, 4, 5, 3, 2, 4, 3, 1, 3], Pearson χ²=7.5941 (8 degrees of freedom), and the approximate p-value 0.4741. Seven of nine expected digit counts are below five; the smallest is about 1.37.

## Limitations
The asymptotic p-value needs caution because of small expected counts. Non-rejection does not prove conformity, and neither conformity nor deviation establishes election integrity. Population and turnout constrain provincial totals, and the appropriateness of the Benford reference model requires justification. The original repository did not document the upstream election-data source.

## Data
Data/Election2009Iran.csv contains 30 provincial rows. Only Total votes is used for the reported test; candidate names and regional labels remain factual source data.

## Verification
Counts and relevant numerical findings were checked independently in Python. R is unavailable here, so revised R code was reviewed but not parsed, executed or rendered. Historical images are retained separately from the revised workflow.

## Run
Install R and Pandoc (or use RStudio), then run from the repository root:
```r
source("install.R")
rmarkdown::render("Notebooks/benford_iran_election.Rmd")
```
Dependencies are unpinned. No API key is needed for the default workflow.

## Files
- [R Markdown analysis](Notebooks/benford_iran_election.Rmd)
- [Readable analysis](Reports/benford_iran_election.html)
- [Portfolio report](https://cameron-batts.github.io/benford_iran_election.html)

## References
- [Deckert, Myagkov and Ordeshook (2011), Benford’s Law and the Detection of Election Fraud](https://doi.org/10.1093/pan/mpr014)
