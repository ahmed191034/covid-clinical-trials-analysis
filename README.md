# COVID-19 Clinical Trials — Exploratory Data Analysis

Exploratory analysis of 5,783 COVID-19 clinical trials registered on ClinicalTrials.gov — trial status, phase, study type, funding source, enrollment size, and a data-quality look at how inconsistently the condition itself is labeled across independently-submitted trials.

**Tools:** Python · pandas · seaborn · matplotlib

## Key Findings

- **5,783** trials analyzed; **~48% (2,805)** were still recruiting at the time of the data pull — this is a live registry snapshot from an active pandemic, not a closed retrospective dataset.
- **Interventional trials (3,322)** outnumber **observational trials (2,427)**; "Not Applicable" is the single largest phase category, reflecting how much COVID-19 research (diagnostics, device trials, observational cohorts) falls outside the standard drug-trial phase system.
- **~78% of trials (4,488)** are funded by non-industry, non-government ("Other") sponsors — consistent with COVID-19 research being driven heavily by academic medical centers reacting fast to an emerging crisis.
- Enrollment is **heavily right-skewed**: mean enrollment is ~18,300, but the median is just **170**. The mean is dragged up by a handful of registry-scale studies (the largest exceeds 20 million participants) — median is the honest number to quote here, and the notebook calls this out explicitly rather than reporting the mean at face value.
- **Data quality finding:** the same disease appears under at least 10 different labels in the `Conditions` field (`Covid19`, `COVID-19`, `COVID`, `Covid-19`, `Coronavirus`, `SARS-CoV-2`, etc.). Naively grouping by `Conditions` would badly undercount COVID-19 trials — this needs a normalization step before any condition-level aggregation can be trusted.

## Files

- `covid_analysis.ipynb` — full analysis notebook
- `COVID clinical trials - COVID clinical trials.csv` — dataset (ClinicalTrials.gov COVID-19 trial registry export)

## Running It

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook covid_analysis.ipynb
```

## What I'd Add Next

- A normalization step for `Conditions` and a re-run of condition-level counts
- A timeline view of trial start dates to show enrollment ramp-up over the pandemic
- A geographic breakdown using the `Locations` field
