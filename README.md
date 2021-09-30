# InfoLing2_Projekt

## Table of contents
* [General info](#general-info)
* [Datasets](#datasets)
* [Classifiers](#classifiers)
* [Python Notebooks](#python-notebooks)
* [Used libraries and packages](#used-libraries-and-packages)
* [Saved Model (RoBERTa)](#saved-model)
* [How to use the tool](#how-to-use-the-tool)
* [Important notes](#important-notes)

## General info:
Abschlussprojekt des Kurses Informationslinguistik 2 an der Universität Regensburg von:
- Julian Högerl, julian.hoegerl@stud.uni-regensburg.de, Matrikel-Nr: 2065797

## Datasets:
Detecting Insults in Social Commentary;. Available from: https://kaggle.com/c/detecting-insults-in-social-commentary.
- .tsv files for classifiers implemented with FARM

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
  - for this notebook you have to use Google Colab
- statistical_analysis.ipynb
  - All statistical analyses and comparisons of the classifiers were performed here
- InfoLing2_Projekt_perform_prediction.ipynb
  - This is where the implementation of the tool takes place, but before that you need a dataset of scraped YouTube comments in csv format
  - I would recommend using Google Colab for this notebook

## Used libraries and packages
- InfoLing2_Projekt_scikit_learn.ipynb
  - scipy: for stats
  - stats: for performing t-tests
  - seaborn: for plotting
  - sklearn: for classifiers
  - pandas: Allows you to quickly and effectively manipulate our datasets through the DataFrame object, as well as read and write data in various formats (CSV, Txt, etc.)
  - re: for cleaning Comments with regex
  - json: to dump results into json-file
  - preprocessor from tweet-preprocessor: for cleaning comments
  - cross_val_score: for computing cross-validation
  - CountVectorizer: for vectorizing comments
  - accuracy_score: for computing accuracy
  - classification_report: not needed for tool but useful for getting quick overview 
  - f1_score: for computing f1_score
  - svm: classifier
  - SVC: needed for svm
  - BernoulliNB: classifier
  - LogisticRegression: classifier 
- InfoLing2_Projekt_FARM.ipynb
  - torch: to fetch the right device
  - farm
    - Tokenizer
    - TextClassificationProcessor
    - DataSilo
    - DataSiloForCrossVal
    - LanguageModel
    - TextClassificationHead
    - AdaptiveModel
    - initialize_optimizer
    - Trainer
    - EarlyStopping
    - set_all_seeds
    - MLFlowLogger
    - initialize_device_settings
    - Evaluator
    - simple_accuracy
    - register_metrics
    - AutoTokenizer
  - scipy: for stats
  - stats: for t-test
  - pandas: Allows you to quickly and effectively manipulate our datasets through the DataFrame object, as well as read and write data in various formats (CSV, Txt, etc.)
  - matthews_corrcoef: for computing different metrics
  - f1_score: for computing different f1-metrics
  - logging: for logging
  - json: for dumping results of cross-validation
  - mlflow: for tracking the experiment
  - Path: for path specifications
  - preprocessor from tweet-preprocessor: for cleaning comments
- statistical_analysis.ipynb
  - json: for reading the saved json-files produced in InfoLing2_Projekt_scikit_learn.ipynb and InfoLing2_Projekt_FARM.ipynb
  - pandas: Allows you to quickly and effectively manipulate our datasets through the DataFrame object, as well as read and write data in various formats (CSV, Txt, etc.)
  - scipy: for stats
  - stats: for performing t-tests
  - seaborn: for plotting
  - matplotlib: only for customizing the produced plots (e.g adding legend)
- InfoLing2_Projekt_perform_prediction.ipynb
  - torch: to fetch the right device
  - farm
    - Inferencer: to apply saved model on dictionary
  - pandas: Allows you to quickly and effectively manipulate our datasets through the DataFrame object, as well as read and write data in various formats (CSV, Txt, etc.)
  - PrettyPrinter: for printing inference result

## Saved Model 
Best fold of RoBERTa
- https://drive.google.com/drive/folders/1nhw2pdpXPxmEGLrN3rP3CQEP-UajSvkE?usp=sharing

## How to use the tool
1. Scraping the comments of a YouTube video<br>
Simply follow the Tutorial of "Learning Orbis": https://www.youtube.com/watch?v=uD58-EHwaeI
2. Upload your created .csv-file into your python environment
3. Set the path to the .csv-file
4. Upload the model into your python environment
5. Set path to model
6. Run the notebook

## Important notes
Mir ist leider relativ spät aufgefallen, dass ich die Daten für die FARM-Klassifikatoren nicht mit der cleaning function in neue csv-Dateien bzw. tsv-Dateien abgespeichert habe. Da das Trainieren und Evaluieren sehr viel Zeit in Anspruch nimmt, bleibt mir dafür auch leider keine Zeit mehr. Ich bitte um entschuldigung.

