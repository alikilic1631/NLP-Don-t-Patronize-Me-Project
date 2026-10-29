## NLP Coursework — Detecting Patronising and Condescending Language (PCL)

NLP coursework for detecting patronising and condescending language in news text.

## Task Description

This project implements a binary classifier for Patronising and Condescending Language (PCL) as defined in SemEval 2022 — Task 4 (Subtask 1).
The prediction files required for submission are:

- dev.txt — predictions for the official dev set
- test.txt — predictions for the official test set

## Approach

- Fine-tune a RoBERTa-base pretrained model.
- Use metadata inserted model inputs to provide additional context.
- Train with class weighted focal loss to address class imbalance.
- Perform threshold tuning on an internal validation split.

## Repository Structure

```text
nlp_cw_2026_ak5323/
├── dev.txt                         # Dev set predictions
├── test.txt                        # Test set predictions
├── NLP - CW Report.pdf             # Coursework report
├── BestModel/
│   └── BestModel.ipynb             # Model implementation & evaluation notebook
├── EDA/
│   ├── EDA.ipynb                   # Exploratory data analysis notebook
│   └── EDA Plots/                  # Saved EDA figures
├── Data/
│   ├── dontpatronizeme_pcl.tsv
│   ├── train_semeval_parids-labels.csv
│   ├── dev_semeval_parids-labels.csv
│   └── task4_test.tsv
└── output/                         # Saved model checkpoints & configs
```

## Running code

Run the full training/evaluation pipeline:

Open and run BestModel/BestModel.ipynb

To reproduce EDA outputs (optional):

Open and run EDA/EDA.ipynb

## Result

On the official dev set, the model achieves an F1 score of 0.60.

## Quick links

- dev.txt — Official dev set predictions
- test.txt — Official test set predictions
- BestModel/BestModel.ipynb — Model training notebook
- EDA/EDA.ipynb — EDA notebook
- NLP - CW Report.pdf — Report
