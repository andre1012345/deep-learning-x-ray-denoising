# Data

This project uses the **NIH ChestX-ray14** dataset (National Institutes of Health Clinical Center).
The images are not included in this repository because of their size and licence.

## Download

From the official NIH page: https://nihcc.app.box.com/v/ChestXray-NIHCC

You need two files:

- `Data_Entry_2017_v2020.csv` – metadata (patient ID, view position, …)
- `images/images_001.tar.gz` – first image archive (~1.9 GB, ~5,000 images)

Place both in a `data/` folder in your Google Drive (the notebook expects `MyDrive/autoencoder_project/data`).

## Preprocessing (done in the notebook)

1. Keep only PA views → 3,290 images.
2. Split by patient ID: 2,274 train / 503 validation / 513 test.
3. Convert to grayscale, resize 1024×1024 → 128×128, normalise to [0, 1].

## Citation

Wang X. et al., *ChestX-ray8: Hospital-scale Chest X-ray Database and Benchmarks on Weakly-Supervised Classification and Localization of Common Thorax Diseases*, CVPR 2017.
