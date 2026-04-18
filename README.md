
🌊 Flood Risk Mapping using Regression SVM Gradient Boosting

##  Overview
This project applies machine learning techniques to predict flood-prone areas in Swat, Khyber Pakhtunkhwa, Pakistan using satellite-derived geospatial data.

The system generates flood risk maps using environmental variables such as elevation, slope, and rainfall.

---

##  Study Area
- Region: Swat Valley, Pakistan  
- Data Type: GeoTIFF Raster Data  
- Platform: Google Colab + Google Drive  

---

##  Dataset Used

The following geospatial datasets were used:

-  Digital Elevation Model (DEM)
-  Terrain Slope
-  CHIRPS Rainfall Data
-  Flood Extent Map (Target Label)

---

##  Machine Learning Models

Three machine learning models were compared:

- 🔵 Logistic Regression  
- 🟣 Support Vector Machine (SVM)  
- 🟢 Gradient Boosting Classifier  

---

##  Results Summary

| Model | Accuracy |
|------|---------|
| Logistic Regression | ~78% |
| SVM | ~78% |
| Gradient Boosting | **~80% (Best Model)** |

###  Best Model:
Gradient Boosting Classifier

---

## Key Findings

- Gradient Boosting performed best due to its ability to capture non-linear relationships.
- SVM performed competitively with good generalization.
- Logistic Regression provided a strong baseline model.

---

##  Important Methodology Note

To avoid data leakage, SAR-derived flood maps were excluded from training.

Only independent variables were used:
- DEM  
- Slope  
- Rainfall  

This ensures a realistic and scientifically valid ML workflow.

---


---

##  Technologies Used

- Python 🐍  
- Scikit-learn  
- Rasterio  
- NumPy  
- Matplotlib  
- Seaborn  
- Google Colab  

---

##  Common Mistakes to Avoid (IMPORTANT)

###  1. Data Leakage
Do NOT use SAR-based flood maps as both input and label source together.

---

###  2. Using Too Small Sample
Avoid:
- very small pixel samples (<10,000)

Use 50,000–100,000 samples for stability

---

###  3. Ignoring Class Imbalance
Flood pixels are usually fewer.

 Always balance dataset properly.

---

###  4. Pixel-wise Random Split Without Sampling
Adjacent pixels are similar → leads to fake high accuracy.

 Always use random sampling.

---

###  5. Overclaiming Accuracy
Do NOT write:
> “Model is highly accurate for real-world forecasting”

Instead write:
 “Model provides moderate predictive performance based on available satellite data.”

---

##  How to Improve This Project Further

###  1. Add more features
- Distance to river
- Land use / land cover (NDVI)
- Soil type

---

###  2. Use advanced models
- XGBoost (already tried but can be improved)
- Random Forest
- Deep Learning (CNN for raster data)

---

###  3. Improve flood detection
- Use class weighting
- Adjust probability threshold (0.3–0.4 instead of 0.5)

---

###  4. Spatial validation
Instead of random split:
- Use region-based split (more realistic)

---

###  5. Deploy project
- Streamlit web app
- GIS dashboard
---

##  Conclusion
This project demonstrates how machine learning can be used for flood risk mapping using geospatial raster data, providing insights for disaster management and planning.

