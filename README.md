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
  - In diesem Notebook wurden SVM, Naïve Bayes und Logistic Regression mit sci-kit learn implementiert
- InfoLing2_Projekt_FARM.ipynb
  - In diesem Notebook wurden alle transformer-basierten Modelle (BERT, DistilBERT, DistilBERT SST2, RoBERTa, ALBERT v2 und XLMRoBERTa) mit FARM implementiert
- statistical_analysis.ipynb
  - Hier wurden alle statistischen Analysen der Klassifikatoren durchgeführt
  - Vergleich zwischen der Baseline und den anderen Klassifikatoren findet ebenfalls hier statt
- InfoLing2_Projekt_perform_prediction.ipynb
  - Hier findet die Implementation des tools statt, zuvor braucht man aber noch einen Datensatz gescrapter YouTube-Kommentare im csv-Format 

## Saved Model (RoBERTa)
- https://drive.google.com/drive/folders/1nhw2pdpXPxmEGLrN3rP3CQEP-UajSvkE?usp=sharing
