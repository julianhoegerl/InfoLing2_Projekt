# InfoLing2_Projekt

## Table of contents
* [General info](#general-info)
* [Datasets](#datasets)
* [Classifiers](#classifiers)

## General info:
Abschlussprojekt des Kurses Informationslinguistik 2 an der Universität Regensburg von:
- Julian Högerl, julian.hoegerl@stud.uni-regensburg.de, Matrikel-Nr: 2065797

## Datasets:
Detecting Insults in Social Commentary;. Available from: https://kaggle.com/c/detecting-insults-in-social-commentary.
- .tsv files for distilbert-base-uncased-finetuned-sst-2-english

## Classifiers:
- Support Vector Machine
- Naïve Bayes
- Logistic Regression
- BERT (Baseline)
- DistilBERT
- DistilBERT base uncased finetuned SST-2
- RoBERTa
- ALBERT v2
- XLMRoBERTa

## Python Notebooks
- InfoLing2_Projekt_scikit_learn.ipynb
  - In this notebook SVM, Naïve Bayes and Logistic Regression were implemented with sci-kit learn.
- InfoLing2_Projekt_FARM.ipynb
  - In this notebook, all transformer-based models (BERT, DistilBERT, DistilBERT SST2, RoBERTa, ALBERT v2 and XLMRoBERTa) were implemented with FARM
- statistical_analysis.ipynb
  - All statistical analyses and comparisons of the classifiers were performed here
- InfoLing2_Projekt_perform_prediction.ipynb
  - This is where the implementation of the tool takes place, but before that you need a dataset of scraped YouTube comments in csv format 

## Saved Model (RoBERTa)
- https://drive.google.com/drive/folders/1nhw2pdpXPxmEGLrN3rP3CQEP-UajSvkE?usp=sharing

## Benutzung des Tools
1. Scraping the comments of a YouTube video<br>
Simply follow the Tutorial of "Learning Orbis": https://www.youtube.com/watch?v=uD58-EHwaeI
2. Upload your created .csv-file into your python environment
3. Set the path of the .csv-file
4. Run the notebook


