# Predicting H1N1 and Seasonal Flu Vaccines

## Project Overview
This project aims to predict the likelihood of individuals receiving the H1N1 and seasonal flu vaccines using survey data about their backgrounds, opinions, and health behaviors. The data comes from the National 2009 H1N1 Flu Survey.

The challenge is to predict two target variables:
- `h1n1_vaccine` — whether the respondent received the H1N1 flu vaccine.
- `seasonal_vaccine` — whether the respondent received the seasonal flu vaccine.

Both are binary variables (`0` = No, `1` = Yes). This is a multilabel classification problem, where individuals may have received none, one, or both vaccines.

---

## Dataset Features
The dataset contains 36 columns:
- `respondent_id`: Unique identifier for each respondent.
- 35 features related to demographics, behaviors, opinions, and health status.

### Examples of Features:
- **h1n1_concern**: Level of concern about the H1N1 flu (0 to 3).
- **behavioral_antiviral_meds**: Whether antiviral medication was taken (binary).
- **doctor_recc_h1n1**: Whether doctor recommended the H1N1 vaccine (binary).
- **opinion_h1n1_vacc_effective**: Opinion on H1N1 vaccine effectiveness (1 to 5).
- **age_group**, **education**, **race**, **sex**, **income_poverty**, and more demographic and health-related features.

(For full list of features, see DATA_DESCRIPTION.qmd documentation.)

---

## Performance Metric
Model performance is evaluated by the **mean ROC AUC** score over the two target variables (`h1n1_vaccine` and `seasonal_vaccine`). ROC AUC measures the ability to rank positive cases higher than negative ones, with values closer to 1 indicating better performance.

