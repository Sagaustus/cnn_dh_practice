# Digital Humanities Text Classification Practice Guide

This repository demonstrates a simple text classification workflow in Keras for students interested in Digital Humanities projects. It contains a small example dataset and step-by-step Jupyter notebooks.

## 1. Repository Structure

```
DH_Text_Classification/
├── data/                  # sample corpus & labels
│   ├── texts.csv          # small set of example texts
│   └── label_map.json     # maps label IDs to author names
├── notebooks/             # one notebook per step
│   ├── 1_install.ipynb    # pip install & imports
│   ├── 2_load_split.ipynb # load CSV, train/test split
│   ├── 3_vectorize.ipynb  # tokenize & pad sequences
│   ├── 4_model.ipynb      # build & compile Keras model
│   ├── 5_train.ipynb      # fit model, plot metrics
│   └── 6_evaluate.ipynb   # evaluate on test set
├── requirements.txt       # tensorflow, scikit-learn, pandas
└── README.md              # this guide
```

## 2. Sample Data (`data/texts.csv`)

The `data` folder contains a tiny CSV with two columns, `text` and `label`. The labels correspond to authors listed in `data/label_map.json`.

```
text,label
"To be, or not to be: that is the question...",0
"Call me Ishmael. Some years ago—never mind how long...",1
"It was the best of times, it was the worst of times.",2
```

`label_map.json`:

```json
{  "0": "Shakespeare",  "1": "Melville",  "2": "Dickens" }
```

## 3. Notebooks Overview

Each notebook focuses on one part of the workflow. Run them in order:

1. **1_install.ipynb** – installs packages and verifies imports.
2. **2_load_split.ipynb** – loads the CSV and splits into train/test sets.
3. **3_vectorize.ipynb** – tokenizes text and pads sequences.
4. **4_model.ipynb** – defines a simple Keras model.
5. **5_train.ipynb** – trains the model and plots accuracy/loss.
6. **6_evaluate.ipynb** – evaluates on the test set and prints a confusion matrix.

## 4. Getting Started

1. Clone or download this repository.
2. `cd DH_Text_Classification`
3. (Optional) create a virtual environment:
   ```bash
   python3 -m venv .venv && source .venv/bin/activate
   ```
4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
5. Launch Jupyter Lab:
   ```bash
   jupyter lab
   ```
6. Open each notebook inside the `notebooks/` folder and run the cells sequentially.

## 5. Next Steps

* Replace the example CSV with your own texts or genres.
* Adjust hyperparameters like vocabulary size or number of epochs.
* Visualize embeddings with TensorBoard.
* Try convolutional layers for character-level models.

Happy learning!
