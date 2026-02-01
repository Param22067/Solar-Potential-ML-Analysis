# ☀️ Solar Energy Potential Mapping: A Machine Learning Approach
**Project for Analytics Club Endterm**

## 📖 Introduction
This project uses a **Random Forest Regressor** to predict Global Horizontal Irradiance (GHI) across Rajasthan, Gujarat, and Maharashtra. It further integrates infrastructure data to produce a Final Suitability Map for solar farm development.

## 🛠️ Tech Stack
* **Language:** Python
* **Platform:** Google Earth Engine (GEE)
* **Libraries:** `geemap`, `ee`, `scikit-learn` (via GEE native classifiers)

## ⚙️ Methodology
1. **Data Acquisition:** Fetching ERA5-Land GHI data and SRTM Digital Elevation Models.
2. **Feature Engineering:** Calculation of Slope and South-Facing Aspect Index.
3. **ML Training:** Stratified sampling of 2000+ points for Random Forest training.
4. **Suitability Overlay:** Weighted combination of:
   - Predicted Solar Potential (40%)
   - Grid Proximity (30%)
   - Road Proximity (20%)
   - Terrain Slope (10%)

## 📊 Key Results
- **Model Accuracy:** R² Score of ~0.66.
- **Top Sites:** Identified Jaisalmer (Rajasthan) and Kutch (Gujarat) as Tier-1 development zones.

## 🚀 How to Run
1. Open `Solar_Suitability_Analysis.ipynb` in Google Colab.
2. Authenticate your Google Earth Engine account when prompted.
3. Run all cells to generate the interactive maps and validation plots.
