# Data

This repository contains the processed datasets used in the final analysis.

The original data were obtained from two publicly available Kaggle datasets. The primary source contains approximately 4.5 million headlines from major online news publications between 2007 and 2022. For this project, the data were filtered to include selected liberal and conservative outlets and headlines related to COVID-19, pandemic response, and vaccination. A second Kaggle dataset was used to obtain vaccine-related headlines from 2024.

## Files

- `filtered_covid_vaccine_headlines.csv`  
  Contains COVID-19 and vaccine-related headlines from 2020–2022 used to analyze ideological differences in pandemic coverage. The final dataset includes 22,520 conservative and 19,741 liberal headlines.

- `filtered_vaccine_headlines_2019.csv`  
  Contains vaccine-related headlines from 2019 used as the pre-pandemic comparison.

- `filtered_vaccine_headlines_2024.csv`  
  Contains vaccine-related headlines from 2024 used as the post-pandemic comparison.

## News Outlets

The primary analysis includes headlines from:

**Liberal**
- CNN
- The New York Times
- The Guardian

**Conservative**
- Fox News
- Daily Mail
- New York Post

Outlet ideology was categorized using the AllSides Media Bias Chart.

## Filtering

COVID-19-related headlines were identified using keywords including terms such as `covid`, `pandemic`, `lockdown`, `quarantine`, `vaccine`, and `booster`.

The 2019 and 2024 vaccine datasets were filtered using broader vaccine-related terms such as `vaccine`, `vaccination`, `immunization`, and `inoculation`. 

## Source Data

The processed files in this repository are derived from publicly available Kaggle datasets. Full source citations and additional details are available in the project report.
