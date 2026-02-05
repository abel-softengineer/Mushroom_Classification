# Mushroom Classification Project

A Python-based machine learning project to classify mushrooms as edible or poisonous using their physical attributes.

## Overview
The goal was to build a reliable classifier using a KNN (K-Nearest Neighbors) approach. The project covers the full pipeline from raw data handling to final predictions on a validation set.

## Project Structure
* `input.csv`: Training dataset.
* `validation.csv`: Independent data for final testing.
* `main.py`: Main script for preprocessing and modeling.
* `pred.txt`: Exported predictions.

## Technical Implementation

### 1. Data Preprocessing
* **Missing Values:** Handled nulls in `cap-diameter` using the median and `ring-type` using the mode (most frequent value).
* **Feature Engineering:**
    * Converted categorical features (`cap-shape`, `cap-color`, `ring-type`) into numerical values using **Ordinal Encoding**.
    * Simplified the `has-ring` column into a binary (1/0) format.
    * Dropped unnecessary or non-numeric columns before training.

### 2. Modeling & Prediction
* Used **Scikit-learn's KNeighborsClassifier** (n_neighbors=5).
* Split the training data into 80% training and 20% testing sets to monitor performance.
* Performed final predictions on the external `validation.csv` file.
* Results are saved as a text file for easy verification.

## Requirements
* Python 3.x
* pandas
* scikit-learn
* numpy

## How to use
1. Clone the repo:
   ```bash
   git clone [https://github.com/abel-softengineer/Mushroom_Classification.git](https://github.com/abel-softengineer/Mushroom_Classification.git)
