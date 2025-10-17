# 🌳 Urban Tree Canopy and Heat Islands in Chicago

**Author:** Utsavi Shah  
**Email:** ups2@illinois.edu  
**Course:** GGIS 407 – Advanced GIS  
**Project:** 5  

---

## 🧩 Project Overview

This project investigates the **relationship between urban tree canopy coverage and the Urban Heat Island (UHI) effect** in the city of Chicago.  
Urban areas often experience higher temperatures than surrounding rural zones, intensifying health risks, energy demands, and infrastructure strain.  

The study **quantifies how green infrastructure — particularly public trees — mitigates urban heat** through shading and evapotranspiration.  
By combining **geospatial and statistical analysis**, this project demonstrates that communities with denser tree coverage experience cooler surface temperatures.

---

## 🗺️ Data Sources and Methodology

**Datasets Used:**
- **Community Areas (Polygons):** Chicago’s 77 official community boundaries.  
- **Tree Inventory (Points):** Over 47,000 public street trees.  
- **Land Surface Temperature (Raster):** Proxy for UHI intensity, representing peak summer LST.  

**Key Steps:**
1. **Spatial Join:** Aggregated tree point data to community polygons to compute tree count and density.  
2. **Exploratory Mapping:** Visualized spatial variation in tree cover and LST to identify potential UHI zones.  
3. **OLS Regression Models:** Quantified statistical relationships between tree metrics and heat intensity.

---

## 📊 Statistical Modeling

### Model 1: Simple OLS Regression  
**Variables:**  
- Dependent: `avg_lst` (Land Surface Temperature)  
- Independent: `tree_count`

**Result:**  
A strong, statistically significant negative correlation.  
**R² = 0.552**, showing that tree count explains over half of the variation in LST.

### Model 2: Multiple OLS Regression  
**Variables:** `avg_lst` ~ `tree_count` + `density`

| Variable | Coefficient | t-Stat | P>|t| | Interpretation |
|-----------|--------------|--------|------|----------------|
| const | 31.965 | 350.7 | 0.000 | Baseline LST |
| tree_count | −0.0010 | −4.94 | 0.000 | Every 1,000 trees reduce LST by ≈ 1°C |
| density | 0.0004 | 0.197 | 0.845 | Not statistically significant |

📉 **Interpretation:** Tree canopy coverage has a strong cooling effect — neighborhoods with more trees are measurably cooler.

---

## 🌡️ Policy Applications and Simulation

### Heat Vulnerability Index (HVI)
HVI = Standardized LST − Standardized Tree Count  
- **Dark Red Areas:** Hotter and tree-poorer — highest priority for intervention.  

### Residuals Map
Identifies where other factors (impervious surfaces, water bodies, industrial heat) influence temperature beyond tree cover.

### Tree Planting Simulation
- **Scenario:** Add 2,500 trees in each of the 7 most vulnerable community areas.  
- **Predicted Cooling:** ≈ 2.5°C temperature reduction.

🗺️ The simulation visualizations highlight clear, location-specific climate benefits from increased urban canopy.

---

## 🧠 Key Takeaways

- Urban tree canopy significantly **reduces heat exposure** across Chicago.  
- Statistical results validate **green infrastructure as a measurable, cost-effective climate adaptation strategy**.  
- Tools like the **HVI and simulation maps** guide equitable investment in heat resilience.

---

## 🛠️ Tools and Techniques
- **ArcGIS Pro** for spatial joins, mapping, and visualization  
- **OLS Regression (ArcGIS / Python)** for statistical modeling  
- **Data Cleaning and Analysis** in Excel and ArcGIS environments  

---

## 📂 Repository Structure

```
├── data/
│   ├── chicago_trees.shp
│   ├── community_areas.shp
│   └── LST_raster.tif
├── maps/
│   ├── tree_count_map.png
│   ├── lst_map.png
│   ├── hvi_map.png
│   └── predicted_lst_reduction.png
├── results/
│   ├── regression_output.csv
│   └── model_residuals.csv
└── README.md
```

---

## 📜 Citation

Shah, U. (2025). *Urban Tree Canopy and Heat Islands in Chicago.*  
University of Illinois Urbana-Champaign, Department of Geography & GIScience.

---

## 🌍 Keywords
Urban Heat Island • Tree Canopy • Climate Resilience • GIS • Spatial Analysis • Chicago • Equity • Green Infrastructure
