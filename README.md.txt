# COVID Clinical Trials Analysis

Exploratory data analysis of global COVID-19 clinical trial records to identify patterns in study status, trial phases, enrollment, study types, sponsorship, and geographic activity.

## Overview

This project explores a dataset of COVID-19 clinical trials to understand how research activity was distributed across different study categories. The analysis focuses on the structure and quality of the dataset, missing-value patterns, trial status distribution, phase-level trends, enrollment behaviour, study types, and leading sponsors.

The aim is to turn raw clinical-trial records into clear and interpretable insights using Python-based exploratory data analysis.

## Objective

The project was designed to answer questions such as:

- Which trial statuses were most common?
- Which clinical trial phases appeared most frequently?
- How does enrollment vary across phases?
- What types of studies dominate the dataset?
- Which institutions appear most often as sponsors or collaborators?
- What does the dataset reveal about active global COVID-19 research activity?

## Why This Project Matters

Clinical trial datasets are often large, text-heavy, and difficult to interpret directly. This project shows how exploratory data analysis can be used to uncover meaningful patterns in healthcare research data and improve the readability of complex public datasets.

It also demonstrates how structured data analysis can support evidence-based reporting in medical and research-focused domains.

## Dataset

The dataset contains **5,783 clinical trial records** and **27 columns**. It includes information such as:

- NCT Number
- Title
- Status
- Conditions
- Interventions
- Sponsor/Collaborators
- Phases
- Enrollment
- Study Type
- Study Designs
- Trial dates
- Locations
- URL

## Key Analytical Areas

The notebook covers:

- initial dataset inspection
- column data types and summary statistics
- missing-value analysis
- duplicate checking
- status distribution analysis
- phase distribution analysis
- average enrollment by phase
- study type breakdown
- sponsor/collaborator concentration
- conditional filtering for selected research insights

## Key Findings

- The dataset contains a broad range of COVID-19 clinical studies, with strong representation of active and planned research.
- Most variables are categorical or text-based, while `Enrollment` is the main numerical feature.
- Missing values are heavily concentrated in `Results First Posted` and `Study Documents`, suggesting that many studies are ongoing or have not yet published formal results.
- `Recruiting` is the most common status, indicating strong ongoing clinical research activity.
- `Not Applicable` is the most common phase category, while `Phase 2` and `Phase 3` are the most common among phased trials.
- Average enrollment generally increases in later phases, which aligns with standard clinical trial progression.
- `Interventional` studies outnumber `Observational` studies in the dataset.
- Large academic hospitals and public healthcare institutions appear frequently among the leading sponsors and collaborators.

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Structure

```text
covid-clinical-trials-analysis/
├── data/
│   └── covid_clinical_trials_analysis.csv
├── notebooks/
│   └── covid_clinical_trials_analysis.ipynb
├── images/
├── outputs/
├── README.md
├── requirements.txt
└── .gitignore