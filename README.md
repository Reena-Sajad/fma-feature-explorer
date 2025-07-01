
# Unsupervised Learning – FMA Dataset Exploration

## Course: CS6140 – Machine Learning (Fall 2024)

### Author: *Reena Sajad Hyder*  

---

## 📌 Objective

This project focuses on exploring the Free Music Archive (FMA) dataset to understand its structure, particularly two key files: `features.csv` and `tracks.csv`. The objective is to analyze the various domains of audio features, interpret track metadata, and plan for integrating these datasets for future unsupervised learning tasks.

---

## 📁 Dataset Overview

The **Free Music Archive (FMA)** dataset is a rich collection of freely available music tracks. It contains:
- **Audio Features**: Extracted characteristics such as MFCCs and chroma representations.
- **Metadata**: Information about each track including title, artist, album, genre, and more.

This assignment explores these two key files:
- `features.csv`: Contains numerical feature vectors extracted from the audio tracks.
- `tracks.csv`: Contains hierarchical metadata for each track.

---

## 🔍 Feature Domains in `features.csv`

The `features.csv` file contains 518 total features grouped into **9 domains**:

| Domain            | Description                                           | Number of Features |
|-------------------|-------------------------------------------------------|---------------------|
| Chroma            | Captures the energy of each pitch class (12-tone scale) | 252                 |
| MFCC              | Mel Frequency Cepstral Coefficients, modeling timbral texture | 140          |
| Spectral Contrast | Measures contrast between spectral peaks and valleys | 42                  |
| Tonnetz           | Tonal centroid features representing harmonic content | 6                   |
| RMS               | Root Mean Square energy of signal                     | 7                   |
| Spectral Centroid| Indicates the “brightness” of a sound                 | 7                   |
| Spectral Bandwidth| Spread of the spectrum                               | 7                   |
| Spectral Flatness| Flatness of the power spectrum                        | 7                   |
| Zero Crossing Rate| Rate of sign-changes in the signal                   | 7                   |

---

## 🧾 Metadata Fields in `tracks.csv`

Selected columns of interest and their descriptions:

| Column        | Description                          |
|---------------|--------------------------------------|
| title         | Name of the track                    |
| artist        | Performing artist                    |
| album         | Album the track is part of           |
| genre_top     | Top-level genre classification       |
| date_created  | When the track metadata was created  |
| license       | Licensing information (e.g., Creative Commons) |
| duration      | Length of the track in seconds       |

---

## 🔗 Data Integration Plan

To prepare for future analysis, a **join strategy** between `features.csv` and `tracks.csv` is proposed:

- Use the **track ID** (available as the index in both files) as the primary key for joining.
- Ensure consistent formatting and ordering of indices.
- Filter to only include tracks with available metadata and valid features to avoid null entries post-join.

---

## 📊 Genre Frequency Distribution

Using `tracks.csv`, the genre distribution is visualized.

This gives insight into the representation of various musical styles in the dataset.

---

## 🛠 Files Included

- `fma-feature-explorer.ipynb` – Main notebook for feature exploration and genre analysis.
- `HW Assignment 4 Unsupervised Learning Part 1.docx` – Assignment instructions.
- `features.csv` – Audio feature matrix.  
- `tracks.csv` – Metadata for each track.

---

## ✅ Summary

This exploratory analysis lays the groundwork for applying unsupervised learning algorithms to music data. By understanding feature distributions, metadata structure, and genre representation, we’re better equipped to tackle clustering or dimensionality reduction in future assignments.
