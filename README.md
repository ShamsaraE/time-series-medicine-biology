# Time Series Analysis in Medicine and Biology

**Practical block course · MSc · University of Tübingen**
Methods in Medical Informatics · PfeiferLab · Department of Computer Science

> Current version: **Wintersemester 2026/27**. Earlier cohorts are available as [tagged releases](../../tags).

<!-- Optional but recommended: add one representative figure to docs/ and uncomment.
     A seasonal decomposition or an STL plot from notebook 01/02 works well. -->
<!-- ![Seasonal decomposition of a biomedical time series](docs/banner.png) -->

A hands-on, two-week intensive course on time-series methods applied to real biomedical
and epidemiological data — mortality, infectious-disease surveillance, multi-omics, and
continuous glucose monitoring. Every method is taught on a real dataset, in Python, with a
worked notebook the same day students apply it to a project.

---

## What you'll learn

By the end of the course you will be able to:

- Decompose biomedical time series into trend, seasonal, and residual components, and decide between **additive and multiplicative** structure
- Read and interpret **autocorrelation (ACF/PACF)** and **spectral (periodogram, FFT/STFT)** structure
- Distinguish **white vs. red (autocorrelated) noise** and handle **missing data** sensibly
- Detect anomalies and epidemic peaks, comparing **Z-score vs. robust MAD** methods
- Build forecasting models — **harmonic regression, ARX with Fourier terms, Ridge / ElasticNet / Random Forest** — and evaluate them honestly with chronological splits, MASE, and seasonal-naive baselines
- Model **seasonality in omics data** with cyclic-spline GAMs
- Reason about **structural breaks** (e.g. how COVID-19 disrupted influenza circulation)

## Prerequisites

Basic Python (NumPy, pandas, matplotlib) and introductory statistics. No prior time-series
background assumed.

---

## Course structure

The course runs as a **two-week block**. Teaching days mix short lectures with worked
example notebooks; students then apply each method to **session projects**, and across the
two weeks develop a larger **final project** presented on the last day.

| | Mon | Tue | Wed | Thu | Fri |
|---|---|---|---|---|---|
| **Week 1** | Teaching | Teaching | Teaching | Final project defined | Final project work |
| **Week 2** | Teaching | Teaching | Final project work | Final project work | **Presentations** |

<!-- Adjust the grid above to match the exact day-by-day plan if it differs. -->

The repository mirrors this in three sections: **teaching notebooks** (worked examples),
**session projects** (guided in-session exercises), and **final projects** (the larger
assessed work).

---

## 1 · Teaching notebooks

Worked examples shown during lectures. Run top to bottom.

| # | Notebook | Topic | Colab |
|---|----------|-------|-------|
| 01 | `teaching/01_uk_respiratory_deaths_structural_model.ipynb` | Structural generative model: additive decomposition, anomaly detection, simulation (UK mortality) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/teaching/01_uk_respiratory_deaths_structural_model.ipynb) |
| 02 | `teaching/02_malaria_cases_multiplicative_model.ipynb` | Multiplicative structure, log transform, classical & STL decomposition (Kericho malaria) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/teaching/02_malaria_cases_multiplicative_model.ipynb) |
| 03 | `teaching/03_uk_respiratory_deaths_deterministic_stochastic_model.ipynb` | Deterministic vs. stochastic modelling of the same series | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/teaching/03_uk_respiratory_deaths_deterministic_stochastic_model.ipynb) |
| 04 | `teaching/04_cgm_hourly_cross_analysis.ipynb` | Cross-analysis of hourly continuous glucose monitoring data | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/teaching/04_cgm_hourly_cross_analysis.ipynb) |
| 05 | `teaching/05_influenza_forecasting_ml.ipynb` | Influenza forecasting with machine-learning models | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/teaching/05_influenza_forecasting_ml.ipynb) |
| 06 | `teaching/06_white_red_noise_missingness.ipynb` | White vs. red (AR(1)) noise, periodograms, missing-data handling | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/teaching/06_white_red_noise_missingness.ipynb) |
| 07 | `teaching/07_arx_model_all_lineages_germany.ipynb` | ARX modelling across SARS-CoV-2 lineages (Germany) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/teaching/07_arx_model_all_lineages_germany.ipynb) |
| 08 | `teaching/08_dominant_frequency_fft_stft_biomedical.ipynb` | Dominant-frequency analysis with FFT and STFT on biomedical signals | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ShamsaraE/time-series-medicine-biology/blob/main/teaching/08_dominant_frequency_fft_stft_biomedical.ipynb) |

<!-- Filenames above assume the renames suggested in the layout section. If you keep the
     current names (e.g. Dominant_Frequency_FFT_STFT_Biomedical.ipynb), update the paths. -->

## 2 · Session projects

Guided exercises students work through during the teaching days, with scaffolding and
questions to answer.

| Notebook | Focus |
|----------|-------|
| `session-projects/01_epidemic_variant_aware.ipynb` | STL on COVID cases (OWID), Z-score vs. MAD anomalies, ECDC variant integration, peak detection |
| `session-projects/02_rki_influenza_germany.ipynb` | RKI influenza by age group, periodogram, temperature coupling, prewhitening, structural break |
| `session-projects/03_seasonality_covid_germany.ipynb` | Spectral period estimation, harmonic regression, Ridge, seasonal-naive baseline, MASE |
| `session-projects/04_dynamic_regression_ridge_elasticnet_rf.ipynb` | Dynamic regression: Ridge / ElasticNet / Random Forest, nested CV, feature importance |

## 3 · Final projects

All students complete both projects across the two weeks. On the final day, half the
class present the first project and half present the second.

| Notebook | Description |
|----------|-------------|
| `final-projects/01_multiomics_seasonality.ipynb` | Seasonal biology in deep longitudinal multi-omics data; insulin-sensitive vs. insulin-resistant groups. Data reconstruction, exploratory seasonal analysis, feature selection, cosine-similarity comparison across omics layers |
| `final-projects/02_rna_gam_model.ipynb` | Cyclic cubic-spline GAM framework for RNA seasonality; genome-wide M0/M1/M2 model comparison via AIC, IR vs. IS seasonal shape |
| `final-projects/03_flusurv_arx.ipynb` | ARX + Fourier model of influenza hospitalization (CDC FluSurv), pooled vs. age-specific models, COVID structural break and interaction effects |

---

## Suggested repository layout

```
teaching/          Worked-example notebooks from lectures (01–08)
session-projects/  Guided in-session exercises
final-projects/    Larger assessed projects (presented on the last day)
data/              Local datasets used by the notebooks
src/               Shared helper functions imported across notebooks (optional)
docs/              Figures used in this README (optional)
```

---

## Getting started

### Option A — Google Colab (no install)

Click any **Colab** badge above. The notebooks load their data either from public URLs
(OWID, RKI, ECDC, Rdatasets) or from the `data/` folder in this repository, so they run in
Colab without setup.

### Option B — Run locally

```bash
git clone https://github.com/ShamsaraE/time-series-medicine-biology.git
cd time-series-medicine-biology
pip install -r requirements.txt
jupyter lab
```

---

## For students

- Work through the **teaching notebooks** in order; each session's **session project**
  applies that day's method.
- You complete **both final projects** across the two weeks; on the last day half the class present the first and half the second.
- Submission and deliverables are described inside each project notebook (clean notebook
  with visible outputs, labelled figures, a short written interpretation).
- <Add: submission channel, office hours, grading weights, contact — or link to the course page>

---

## Data sources

Public datasets used across the course:

- **OWID** COVID-19 data — cases, deaths, stringency, vaccination
- **RKI** influenza surveillance (Germany)
- **ECDC** respiratory-virus variant proportions
- **CDC FluSurv-NET** influenza hospitalization
- **Rdatasets** UK monthly respiratory deaths
- **Kericho** malaria surveillance
- **Open-Meteo** historical temperature

Please cite the original data providers when you reuse these materials.

---

## Citation

If you use these materials, please cite:

> E. Shamsara, *Time Series Analysis in Medicine and Biology* (course materials),
> University of Tübingen, 2026. https://github.com/ShamsaraE/time-series-medicine-biology

---

## License

Released under the [MIT License](LICENSE). Datasets remain under their original licenses.

## Contact

Elham Shamsara — <elham.shamsara@uni-tuebingen.de>
PfeiferLab, Methods in Medical Informatics, University of Tübingen
