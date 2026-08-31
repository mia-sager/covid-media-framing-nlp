# Framing COVID-19 Response and Vaccines Across Ideologies

## Overview

This project analyzes more than **42,000 COVID-19-related news headlines** from six major U.S. news outlets using natural language processing and machine learning to examine how political ideology influenced pandemic and vaccine framing.

The analysis compares liberal and conservative news coverage, tracks changes in language throughout the COVID-19 pandemic, and examines how broader vaccine-related media coverage changed before and after the pandemic.

This project was completed with Molly Murphy for **QTM 340: Data Science of Text at Emory University**.

---

## Research Questions

1. How do conservative and liberal news outlets frame COVID-19 vaccination and pandemic response differently?
2. How did these framing patterns evolve from 2020 through 2022?
3. Did broader media coverage of vaccines change after the COVID-19 pandemic?

---

## Data

The primary analysis uses **42,261 COVID-19-related headlines** published between 2020 and 2022.

### Liberal Outlets
- CNN
- The New York Times
- The Guardian

### Conservative Outlets
- Fox News
- Daily Mail
- New York Post

The headlines were extracted from a publicly available Kaggle dataset containing approximately **4.5 million news headlines** and filtered using COVID-19 and vaccination-related keywords.

A second dataset was used to compare vaccine-related coverage in **2019 and 2024**.

Processed datasets used in the analysis are available in the [`data/`](data/) folder.

---

## Methods

The project combines several natural language processing and machine-learning techniques:

- **TF-IDF Vectorization**
- **Unigram and Bigram Analysis**
- **Logistic Regression Classification**
- **Word2Vec Word Embeddings**
- **Cosine Similarity**
- **Log-Odds Ratios**
- **Temporal Semantic Analysis**

The combination of supervised classification and semantic analysis allowed us to examine both which terms distinguished ideological groups and how the meaning and context of important pandemic-related concepts changed over time.

---

## Key Findings

### 1. Liberal and conservative outlets emphasized different themes

TF-IDF and logistic regression identified distinct language patterns across ideological groups.

Liberal outlets tended to emphasize **scientific developments and situational updates**, while conservative outlets more frequently emphasized **political figures, government authority, and political conflict**.

---

### 2. Policy-related language appeared in different semantic contexts

Separate Word2Vec models were trained on liberal and conservative headlines.

For example, liberal coverage associated **"mandate"** with administrative and public-health language, while conservative coverage associated it more strongly with rights-oriented and oppositional terms.

These differences suggest that the same pandemic-related concepts were discussed within different rhetorical contexts across ideological groups.

---

### 3. Headlines became more distinguishable by ideology over time

Separate TF-IDF logistic regression classifiers were trained for each year of the pandemic.

| Year | Classification Accuracy |
|------|------------------------:|
| 2020 | 0.78 |
| 2021 | 0.81 |
| 2022 | 0.82 |

The increase in classification accuracy suggests that ideological differences in headline language became more pronounced as the pandemic progressed.

---

### 4. Vaccine coverage changed after the COVID-19 pandemic

Vaccine-related headlines from **2019 and 2024** showed a noticeable shift in dominant topics.

Pre-pandemic coverage focused heavily on:
- Measles outbreaks
- Anti-vaccination movements
- Vaccine misinformation

Post-pandemic coverage increasingly focused on:
- COVID-19
- Flu
- Polio
- Mpox
- Ongoing infectious-disease threats

Log-odds analysis also revealed differences in the types of vaccine-related language disproportionately used by liberal and conservative outlets.

---

### 5. Semantic polarization unexpectedly decreased after the pandemic

Despite continued differences in framing and emphasis, the final analysis found that semantic distance between liberal and conservative vaccine-related coverage decreased from **0.059 in 2019 to 0.048 in 2024**.

One possible explanation is that the COVID-19 pandemic introduced a more universal vaccine-related vocabulary, including terms such as *booster*, *variant*, and *dose*.

---

## Repository Structure

```text
covid-media-framing-nlp/
│
├── README.md
│
├── data/
│   ├── README.md
│   ├── filtered_covid_vaccine_headlines.csv
│   ├── filtered_vaccine_headlines_2019.csv
│   └── filtered_vaccine_headlines_2024.csv
│
├── notebooks/
│   └── covid_media_framing_analysis.ipynb
│
├── figures/
│   └── project visualizations
│
├── report/
│   └── Sager_Murphy_Final_Report.pdf
│
└── requirements.txt
```

---

## Running the Analysis

The complete analysis is available in:

[`notebooks/covid_media_framing_analysis.ipynb`](notebooks/covid_media_framing_analysis.ipynb)

The notebook uses the processed datasets stored in the [`data/`](data/) directory.

To install the required Python packages:

```bash
pip install -r requirements.txt
```
---

## Limitations

This analysis uses **news headlines rather than full articles**, which limits the amount of contextual information available.

The selected publications represent only a subset of the broader U.S. media landscape, and keyword-based filtering may exclude relevant coverage.

The results should therefore be interpreted as evidence of patterns in media framing rather than definitive measures of ideological bias.

---

## Collaboration

This project was completed by **Mia Sager and Molly Murphy** as part of QTM 340 at Emory University.

---

## Full Report

The full research paper, including methodology, results, references, and additional figures, is available in the [`report/`](report/) folder.
