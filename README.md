# Toxic Comment Demo

A small demo repo for detecting toxic comments using a simple machine learning pipeline. This repository contains example code to preprocess text, train a classifier, and run inference on new comments.

## Features

- Example preprocessing (tokenization, cleaning)
- Training script for a baseline classifier (Logistic Regression / simple neural net)
- Example inference script to classify single comments or a batch
- Evaluation scripts and sample metrics

## Requirements

- Python 3.8+
- pip

Install dependencies:

```bash
pip install -r requirements.txt
```

## Quick start

1. Prepare data: place a CSV with columns `comment_text` and `toxicity` (0/1) in `data/`.
2. Train a model:

```bash
python train.py --data data/train.csv --output models/baseline.pkl
```

3. Run inference on a single comment:

```bash
python predict.py --model models/baseline.pkl --text "You are amazing!"
```

4. Evaluate on a test set:

```bash
python evaluate.py --model models/baseline.pkl --data data/test.csv
```

## Project structure

- `data/` – dataset CSVs (not included)
- `notebooks/` – example notebooks for exploration
- `src/` – preprocessing, model, and utility code
- `models/` – saved model artifacts
- `requirements.txt` – Python dependencies

## Notes on data & licensing

This repo does not include any copyrighted dataset. When using public datasets (e.g., Jigsaw Toxic Comment), please follow their license and attribution requirements.

## Contributing

Contributions are welcome — open an issue or pull request.

## License

Specify your license here (e.g., MIT).
