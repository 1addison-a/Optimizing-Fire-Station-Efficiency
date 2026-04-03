# Optimizing-Fire-Station-Efficiency
🔥 Fire Station Efficiency Analysis

Bryan Tran · Addison Amadi
UNC Charlotte — Undergraduate Research

📌 Overview

Geospatial analysis of Charlotte fire incidents (2021–2025) to evaluate station coverage efficiency and identify spatial mismatches between demand and response infrastructure.

Core approach: model incident demand → station allocation using optimal transport.

🧰 Tech Stack
Python (pandas, geopandas, matplotlib)
Spatial: pyproj, contextily
Optimization: POT (Python Optimal Transport)
📂 Structure
.
├── Undergrad_Research_Rewrite.ipynb
├── CFD_incidents.csv
├── Current_CFD_Fire_Stations.csv
└── README.md

⚙️ Setup
pip install pandas geopandas matplotlib contextily pyproj pot
jupyter notebook Undergrad_Research_Rewrite.ipynb

🔄 Pipeline
Ingest — ArcGIS API → incident dataset
Clean — timestamps, filtering, validation
EDA — temporal + spatial distributions
Geo Processing — reprojection (EPSG:2264 → 3857)
Modeling — optimal transport for demand allocation
Analysis — detect over/under-served regions

📊 Outputs
Incident density maps
Station vs. demand overlays
Transport-based efficiency insights
Coverage gap identification

⚠️ Assumptions
Uniform station capacity
Euclidean distance (no road network)
Static demand (no forecasting)

🚀 Next Steps
Network-based travel times
Capacity-constrained optimization
Demand prediction models
Station placement optimization
