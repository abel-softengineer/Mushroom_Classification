# Mushroom Classification using KNN

This project focuses on classifying mushrooms as either **edible** or **poisonous** based on their physical characteristics. It implements a Machine Learning workflow using **Python** and **Scikit-learn**.

## 📊 Project Overview
The dataset used contains samples of 23 species of gilled mushrooms. Each species is identified as definitely edible, definitely poisonous, or of unknown edibility and not recommended (combined with poisonous).

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** * `pandas` & `numpy` (Data manipulation)
    * `scikit-learn` (Machine Learning & Preprocessing)
    * `matplotlib` & `seaborn` (Visualization)

## ⚙️ Workflow
1. **Data Cleaning:** Handling missing values and inspecting the dataset structure.
2. **Feature Engineering:** * Applied **Ordinal Encoding** to transform categorical features into numerical format.
    * Feature scaling to ensure the distance-based KNN algorithm performs optimally.
3. **Modeling:** * Implemented the **K-Nearest Neighbors (KNN)** classifier.
    * Split the data into training and testing sets (e.g., 80/20 split).
4. **Evaluation:** Measured performance using accuracy scores and a confusion matrix.

## 🚀 Usage
To run the project locally, clone the repository and install the requirements:

```bash
git clone [https://github.com/abel-softengineer/Mushroom_Classification.git](https://github.com/abel-softengineer/Mushroom_Classification.git)
cd Mushroom_Classification
pip install -r requirements.txt
python main.py
