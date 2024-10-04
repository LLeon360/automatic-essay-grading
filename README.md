# Automated Essay Scoring 

These notebooks were made for the Learning Agency Lab Automated Essay Scoring 2 dataset. The Kaggle comp can be found here (https://www.kaggle.com/competitions/learning-agency-lab-automated-essay-scoring-2).

# Overview

The Deberta notebook finetunes a DebertaV3 Transformer model on the input essays and directly predicts the output score. 
The Engessay model is a transfer learning model trained on the English Language Learner Insight, Proficiency, and Skills Evaluation (ELLIPSE) Corpus.

The Engessay model is a Roberta model that outputs intermediate scores that represent the breakdown of the essay's quality along several English quality metrics:
Example output:
cohesion: 3.5
syntax: 3.5
vocabulary: 4.0
phraseology: 4.0
grammar: 4.0
conventions: 3.5

These direct DebertaV3 and Engessay predictions are combined into a feature dataset to train a XGBoost model and MLP.
This is done in the features dataset notebook and then xgboost notebook.

## Very messy/informal slides for the project with some visualizations
https://docs.google.com/presentation/d/1iFG69ASYLmdwq3Y5WroLS211-PnzACmBj1S7W13TrN4/edit#slide=id.g2e267d4a200_25_104
