# Data

## Station Data
`Current_CFD_Fire_Stations.csv` is included in this folder. It contains
the geographic locations of all 43 active Charlotte Fire Department stations
as of the 2024 operational year.

| Column | Description |
|---|---|
| X | Easting coordinate (NC State Plane, EPSG:2264) |
| Y | Northing coordinate (NC State Plane, EPSG:2264) |
| OBJECTID | Internal feature identifier |
| NUM | Station number |
| NAME | Station name |
| ADDRESS | Station street address |

## Incident Data
`CFD_incidents.csv` is **not included** in this repository. The incident
dataset is not available for public redistribution and has been excluded
from version control.

To reproduce the full analysis, access to Charlotte Fire Department
incident records for 2021–2025 is required. Those looking to apply this
framework to a different city would need to contact their local fire
department to request equivalent incident data.

### Expected Schema
| Column | Description |
|---|---|
| ObjectID | Internal feature identifier |
| IncID | Incident identifier |
| TritechID | Dispatch system identifier |
| FiscalYear | Fiscal year of the incident |
| Latitude | Incident latitude (WGS 84) |
| Longitude | Incident longitude (WGS 84) |
| IncidentDate | Timestamp of the incident |
| CFAI_IncBucket | Incident category classification |
| NFIRSCode_Description | NFIRS incident type description |
| EmergencyPriority | Priority level of the incident |
| Jurisdiction | Responding jurisdiction |
| ReportIsLocked | Report lock status |

## Synthetic Sample
A synthetic sample dataset mimicking the structure of the incident data
is available in `data/sample/` for testing and demonstration purposes.
Real incident locations are not used in the synthetic data.
