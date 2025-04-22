 **Music Popularity Prediction** 
## Summary  
This project implements a machine‑learning pipeline to **forecast music track popularity** using Python and audio‑feature data from Spotify. It leverages intrinsic sonic attributes—danceability, energy, valence, and more to train a **RandomForestRegressor** that estimates a track’s popularity score (0–100). An interactive **Gradio** interface allows users to input feature values and receive an immediate popularity prediction locally.

---

## Overview  
Music popularity prediction applies regression techniques to audio and metadata features to estimate listener engagement metrics.  
Accurate forecasts help streaming platforms optimize playlists, enhance recommendation systems, and boost user satisfaction by prioritizing likely hits.

---

## Dataset  
- **Source**: Spotify‑derived CSV with ~227 tracks, including features such as **danceability**, **energy**, **loudness**, **speechiness**, **acousticness**, **instrumentalness**, **liveness**, **valence**, and **tempo**.  
- **Popularity Label**: Numeric score (0–100) reflecting overall listener interactions citeturn0search0.  
- **Access**: Original data and exploratory analysis available in `notebook.ipynb` following Aman Kharwal’s tutorial.

---

## Project Structure  
```
├── notebook.ipynb          # Data exploration, preprocessing & model training
├── dataset                 # Spotify Dataset
└── README.md               # Project documentation
```  
This layout cleanly separates code, data artifacts, and documentation.

---

## Model Training  
1. **Load data** using `pandas.read_csv()` to read the CSV into a DataFrame citeturn0search1.  
2. **Preprocess**: handle missing values, encode categorical keys, and standardize numeric features.  
3. **Split** into training and test sets with `train_test_split()` (default 75/25 split) citeturn0search4.  
4. **Hyperparameter tuning** via `GridSearchCV` over parameters such as `n_estimators`, `max_depth`, and `min_samples_leaf` .  
5. **Train final model**: fit `RandomForestRegressor(random_state=42)` on the training set and serialize to `model.pkl` for inference.

---

## Dependencies  
```text
pandas>=1.0            # Data loading & manipulation 
numpy>=1.19            # Numerical computations 
scikit-learn>=1.0      # ML model & utilities 
gradio>=3.0            # Web demo interface 
```

---

## Contributing  
1. Fork the repository  
2. Create a feature branch: `git checkout -b feature/xyz`  
3. Commit your changes: `git commit -m "Add feature xyz"`  
4. Push to GitHub and open a Pull Request

---
