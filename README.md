
# IEAP – RStudio Series 03

**Data Wrangling and ANOVA** | Master 1 IEAP, Université de Montpellier

## Project overview

This group assignment uses R to study how **movement time** changes as **task difficulty (Index of Difficulty, ID)** increases. We compare three groups using data from a study on movement after stroke:

- `ap` — healthy adults
- `cp` — healthy young participants
- `pp` — participants with stroke

**Main question:** Does increasing task difficulty affect movement time differently across the three groups?

## What we did

1. **Cleaned the data:** Checked missing conditions and kept `ID1`, `ID2`, `R1`, and `R2` for consistent comparisons.
2. **Ran a mixed-design ANOVA:** Tested the effects of group, difficulty, and their interaction on movement time.
3. **Ran linear regressions:** Calculated a separate movement-time-versus-difficulty equation for each group.
4. **Created figures:** Visualized the interaction and group trends, including variability and regression lines.

## Main findings

- Movement time increased with task difficulty in all three groups.
- The increase was **larger in the stroke group** than in the healthy groups.
- The mixed-design ANOVA found a significant **GROUP × ID interaction** (*p* < 0.001).

## Repository structure

```text
IEAP-Series03-RStudio/
├── IEAP-Series03-RStudio.qmd    # Main Quarto report
├── IEAP-Series03-RStudio.pdf    # PDF report
├── IEAP-Series03-RStudio.Rproj  # RStudio project
├── data/
│   └── Results.csv             # Original dataset
└── sections/
    ├── 01-question-and-method.qmd
    ├── 02-data-preparation.qmd
    ├── 03-anova-analysis.qmd
    ├── 04-regression-and-figure.qmd
    └── 05-discussion.qmd
```

## How to run

1. Open `IEAP-Series03-RStudio.Rproj` in **RStudio**.
2. Install the required R packages:
   ```r
   install.packages(c("tidyverse", "ez", "rstatix"))
   ```
3. Open `IEAP-Series03-RStudio.qmd` and render it with **Quarto** to generate the report. PDF output also requires a working LaTeX installation.

## Contributors

- **Jennifer Houmard** — data preparation, regression, and final figure
- **Valentin Balbine** — mixed-design ANOVA and interaction plots
- **Shakir Nasir** — research question, analysis method, and discussion

The group used separate Git branches for each section before merging the work into `main`.

## Reference

Mottet, D., van Dokkum, L. E. H., Froger, J., Gouaïch, A., & Laffont, I. (2017). *Trajectory formation principles are the same after mild or moderate stroke*. PLOS ONE, 12(3), e0173674. https://doi.org/10.1371/journal.pone.0173674

## License

GNU General Public License v3.0 — see [LICENSE](LICENSE).
