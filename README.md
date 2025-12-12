# Predictive Modeling of Patient Satisfaction: An NLP Analysis of Drug Reviews

**Author:** Xiyuan Du

**Course:** BMIN 5030 

## Research Question
**Can we predict treatment satisfaction and identify the determinants of discontinuation based solely on unstructured patient narratives?**

This project applies Natural Language Processing (NLP) to extract adverse event signals from text and uses Machine Learning to predict whether a patient will be satisfied with their medication.

## Project Files
This repository contains the complete analysis and source code:
* **drug_analysis.html**: The rendered report containing all code, visualizations, and comments.
* **drug_analysis.qmd**: The source of originally R code.
* **drugLibTrain_raw.tsv** / **drugLibTest_raw.tsv**: The raw datasets.

## Dataset
**Source:** drugLib Database
* Selected for its semi-structured format which explicitly separates "Side Effects" text from "Benefits" text.
* The sample size exceeds typical FDA Phase III Clinical Trial enrollment, providing robust statistical power for signal detection.

## Methodology
1.  **Data Processing:** Merged training/testing splits and handled missing categorical values.
2.  **Exploratory Analysis (EDA):** Visualized the "Efficacy-Safety Trade-off" to identify a high-risk cluster of patients reporting high efficacy but severe side effects.
3.  **Natural Language Processing (NLP):** Implemented a tokenization pipeline with a Domain-Specific Stop-Word Filter to remove noise (e.g., "pill", "dosage") and isolate true clinical symptoms.
4.  **Machine Learning:** Trained a Logistic Regression Classifier to predict "Satisfaction" (Rating >= 8) based on a calculated clinical sentiment score.
5.  **Evaluation:** Validated model performance using an ROC Curve.

## Key Findings
The analysis reveals that "Lifestyle Burdens" (e.g., Nausea, Weight Gain, Libido) are the dominant drivers of negative sentiment. The model successfully discriminates between satisfied and unsatisfied patients based on these specific text features.


<!-- Links -->
[forking]: https://guides.github.com/activities/forking/

