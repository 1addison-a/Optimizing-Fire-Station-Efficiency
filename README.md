# Optimizing Fire Station Efficiency
**Bryan Tran · Addison Amadi**
UNC Charlotte — Undergraduate Research | Mentor: Xingjie Li

---

## Overview
Growing up watching Charlotte expand outward in real time, and spending
freshman year getting evacuated from a dorm at 2am every time someone
burnt popcorn, you start to actually wonder — how fast do those trucks
get here, and are the stations even in the right places anymore? That
question turned out to have a rigorous mathematical answer. This project
applies Optimal Transport, a framework originally built to solve abstract
resource allocation problems, to four years of real Charlotte Fire
Department incident records to evaluate whether the city's 43 fire
stations are spatially aligned with where emergencies actually occur —
and to quantify exactly where they are not.

> Full methodology described in the accompanying research report.

---

## Tech Stack
| Area | Libraries |
|---|---|
| Data | pandas, geopandas |
| Visualization | matplotlib, contextily |
| Spatial | pyproj (EPSG:2264 — NAD83 NC State Plane) |
| Optimization | [POT: Python Optimal Transport](https://pythonot.github.io/) v0.9.5 |

---


## Setup
```bash
pip install -r requirements.txt
jupyter notebook notebooks/Undergrad_Research_Rewrite.ipynb
```

**requirements.txt**
```
pot==0.9.5
pandas
geopandas
matplotlib
contextily
pyproj
jupyter
```

---

## Data
The CFD incident dataset was provided directly by the Charlotte Fire
Department for research purposes and is **not included in this repository**.
Station location data (`Current_CFD_Fire_Stations.csv`) is included.

To reproduce results, contact the Charlotte Fire Department directly or
refer to `data/README.md` for the expected schema and a synthetic sample
dataset you can use to run the pipeline end to end.

---


## Next Steps
- Road-network travel times via OSRM
- Heterogeneous station capacity weights proportional to apparatus count
- Severity-adjusted incident demand using NFIRS type codes
- Weekly and daily OT resolution for stations near dynamic demand generators
- Statistical correlation analysis of efficiency drivers
- Station placement optimization for projected demand growth

---

## Citation
If you use this work, please cite:

Tran, B. & Amadi, A. (2025). *Optimizing Fire Station Efficiency*.
UNC Charlotte Undergraduate Research.

POT library (software):
Flamary R., Vincent-Cuaz C., Courty N., Gramfort A., Kachaiev O., Quang Tran H.,
David L., Bonet C., Cassereau N., Gnassounou T., Tanguy E., Delon J., Collas A.,
Mazelet S., Chapel L., Kerdoncuff T., Yu X., Feickert M., Krzakala P., Liu T.,
Fernandes Montesuma E. POT Python Optimal Transport (version 0.9.5).
URL: https://github.com/PythonOT/POT

POT library (paper):
Flamary R., Courty N., Gramfort A., Alaya M.Z., Boisbunon A., Chambon S.,
Chapel L., Corenflos A., Fatras K., Fournier N., Gautheron L., Gayraud N.T.H.,
Janati H., Rakotomamonjy A., Redko I., Rolet A., Schutz A., Seguy V.,
Sutherland D.J., Tavenard R., Tong A., Vayer T. POT Python Optimal Transport
library. Journal of Machine Learning Research, 22(78):1-8, 2021.
URL: https://pythonot.github.io/
