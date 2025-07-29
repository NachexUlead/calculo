# Clustering Penguins in Antarctica

This project applies unsupervised machine learning techniques (K-Means Clustering) to identify natural groupings or potential species of penguins based on morphological features collected by researchers in Antarctica.

---

## Project Overview

A team of researchers collected data on penguins at Palmer Station, Antarctica, as part of the Long-Term Ecological Research (LTER) program. Although the species of each penguin was not recorded, it is known that at least three species inhabit the region: Adelie, Chinstrap, and Gentoo.

Your task as a data scientist is to use clustering techniques to uncover patterns or groups in the dataset that may correspond to these species.

---

## Dataset

The dataset was originally collected by Dr. Kristen Gorman and is provided in CSV format as `penguins.csv`.

**Available columns:**

| Column               | Description                 |
|----------------------|-----------------------------|
| `culmen_length_mm`   | Culmen length (mm)          |
| `culmen_depth_mm`    | Culmen depth (mm)           |
| `flipper_length_mm`  | Flipper length (mm)         |
| `body_mass_g`        | Body mass (g)               |
| `sex`                | Penguin sex (M/F)           |

---

## Technologies and Libraries

- Python
- Pandas
- Matplotlib
- Scikit-learn

---

## Analysis Workflow

1. **Load the dataset** from `penguins.csv`.
2. **Preprocessing:**
   - Convert categorical variables into dummy variables.
   - Standardize numerical features using `StandardScaler`.
3. **Determine the optimal number of clusters** using the Elbow Method.
4. **Apply K-Means Clustering** with the optimal number of clusters.
5. **Visualize the results** (e.g., cluster vs. culmen length).
6. **Compute statistics** for each cluster group.

---

## Results

Four clusters were selected based on the Elbow Method, which evaluates the inertia of each model. The clustering results help visualize how penguins group based on culmen length and other features.

Example visualization:
- Scatter plot of `culmen_length_mm` vs. cluster labels.

---

## output

The project produces a final DataFrame called `stat_penguins`, containing the mean values per cluster for the following columns:

- `culmen_length_mm`
- `culmen_depth_mm`
- `flipper_length_mm`
- `label`

---

## How to Run

1. Make sure Python and the following libraries are installed:
   ```bash
   pip install pandas matplotlib scikit-learn

2. Place the penguins.csv file in the same directory as the script.

3. Run the Python script or execute it step-by-step in a Jupyter Notebook.
