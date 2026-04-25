# Benford's Law Analysis: 2009 Iranian Election Data

**Tools:** R · benford.analysis · tidyverse · ggplot2 · Chi-squared Test

---

## Problem

Following the 2009 Iranian presidential election, widespread allegations of voter fraud prompted protests across the country. The question was whether reported vote totals showed statistical patterns inconsistent with naturally occurring numbers.

## Approach

Applied Benford's Law in R using the benford.analysis package to analyze the leading digit distribution of total vote counts across all regions. Cleaned and tidied the raw election CSV using read_csv, then ran a chi-squared goodness-of-fit test to quantify deviation from expected distributions.

## Impact

The chi-squared test produced a p-value of 0.4741, indicating vote totals did not significantly deviate from Benford's Law, providing a statistically grounded perspective on the fraud allegations using mathematical forensics.

---

## Files

| File | Description |
|------|-------------|
| `benford_iran_election.Rmd` | R Markdown source file with full analysis |
| `benford_iran_election.html` | Rendered HTML output |

---

*Part of my data & analytics portfolio — [cameronbatts.github.io](https://cameronbatts.github.io)*
