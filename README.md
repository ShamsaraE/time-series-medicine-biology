# Time Series Analysis in Medicine and Biology

**Practical course · MSc · University of Tübingen**
Methods in Medical Informatics · PfeiferLab · Department of Computer Science

> Current version: **Wintersemester 2026/27**. Earlier cohorts are available as [tagged releases](../../tags).

<!-- Optional: a single representative figure makes the repo look alive.
     Add one (e.g. a seasonal decomposition or ECG segmentation) to docs/ and reference it: -->
<!-- ![Example: seasonal decomposition of a biomedical signal](docs/banner.png) -->

---

## What you'll learn

By the end of this course you will be able to:

- <e.g. decompose a biomedical time series into trend, seasonal, and residual components>
- <e.g. diagnose autocorrelation structure using ACF/PACF plots>
- <e.g. build and evaluate forecasting models on clinical/biological data>
- <e.g. reason about additive vs. multiplicative dynamics in real signals>
- <add/trim to match your actual learning outcomes>

## Topics

- Trend and seasonality
- Additive vs. multiplicative dynamics
- Autocorrelation and partial autocorrelation (ACF / PACF)
- Decomposition methods
- Forecasting models
- Biomedical case studies

---

## Notebooks

| # | Notebook | Topic | Open in Colab |
|---|----------|-------|---------------|
| 1 | `notebooks/01_<name>.ipynb` | <Introduction & setup> | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/notebooks/01_<name>.ipynb) |
| 2 | `notebooks/02_<name>.ipynb` | <Trend & seasonality> | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/notebooks/02_<name>.ipynb) |
| 3 | `notebooks/03_<name>.ipynb` | <ACF / PACF> | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/notebooks/03_<name>.ipynb) |

<!-- Add one row per notebook. After renaming the repo, the URLs above already point to the new name. -->

---

## Repository structure

```
notebooks/   Teaching notebooks (run top to bottom)
data/        Example datasets used in the notebooks
Projects/    Exercises and project descriptions
src/         Reusable helper functions imported by the notebooks
```

<!-- NOTE: your current README mentions src/ but it isn't in the repo yet.
     Either add it, or delete this line and the src/ row above. Keep them consistent. -->

---

## Getting started

### Option A — Google Colab (no install)

Click any **Open in Colab** badge above. Datasets load directly from this repository, so nothing to set up.

### Option B — Run locally

```bash
git clone https://github.com/ShamsaraE/time-series-medicine-biology.git
cd time-series-medicine-biology
pip install -r requirements.txt
jupyter lab
```

<!-- Make sure requirements.txt actually exists in the repo root — the install line
     currently points to a file that isn't there. A minimal one might be:
     numpy, pandas, matplotlib, statsmodels, scikit-learn, jupyterlab -->

---

## For students

- Work through the notebooks in order; each builds on the previous.
- Exercises and the course project live in `Projects/`.
- <Add: how/where to submit, office hours, grading, contact — or link to the course page>

---

## Citation

If you use these materials, please cite:

> E. Shamsara, *Time Series Analysis in Medicine and Biology* (course materials),
> University of Tübingen, <year>. https://github.com/ShamsaraE/time-series-medicine-biology

---

## License

Released under the [MIT License](LICENSE).

## Contact

Elham Shamsara — <elham.shamsara@uni-tuebingen.de>
PfeiferLab, Methods in Medical Informatics, University of Tübingen
