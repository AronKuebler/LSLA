# Master Thesis: The Impact of LSLA on Social Conflict in Africa  
*Aron Kübler*

---

## Project Description

This Master Thesis investigates the impact of Large Scale Land Acquisitions (LSLA) on social conflict in Africa between 2003 and 2018. The research examines whether the expansion of LSLA activities is associated with increased incidents of social unrest and conflict, considering both environmental and socioeconomic factors. By integrating multiple data sources and applying various statistical methods, the project aims to provide robust evidence on the LSLA–conflict nexus.

---

## Required Files

The file **"LSLA on social conflict"** contains the following folders:
- `a_microdata`
- `b_metadata`
- `c_program`
- `d_results`

*Generally, all files have to be loaded into the folder "b_metadata".*

---

## 1. Afrogrid Dataset

[Afrogrid Dataset on Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/LDI5TK)
- Download **Afrogrid V2.zip**
- Insert **Afrogrid_v2_20220113**

---

## 2. PRIO Grid Datasets

[PRIO GRID DATA Download](https://grid.prio.org/#/download)
- **Download static variables:**
  - Total land area (change name to "PRIO-landarea")
  - Agriculture land (Globcover) (change name to "PRIO-agriland")
- **Download yearly variables:**
  - Distance to capital (2014 - 2014) (change name to "PRIO-GRID Distance Capital")

---

## 3. Large Scale Land Acquisitions

[Large Scale Land Acquisitions on Land Matrix](https://landmatrix.org/map/)
- Select the following:
  - **Land Matrix region:** Africa
  - **Deal size:** 200 -
  - **Negotiation status:** Concluded
  - **Year of initiation:** 2003-2018
  - **Intention of investment:** not no information
- Click download as **xlsx** (file called "export")
- Rename export to "LSLA"

---

## 4. Standardised Precipitation Evapotranspiration Index (SPEI)

[SPEI Data](https://digital.csic.es/bitstream/10261/364137/1/spei01.nc)
- Insert spei01.nc
---

## 5. Arable Land TIF File

[Arable Land Data on ESA](https://due.esrin.esa.int/files/Globcover2009_V2.3_Global_.zip)
- Insert **GLOBCOVER_L4_200901_200912_V2.3**

---

## 6. Nighttime Lights

[Nighttime Lights Dataset on Figshare](https://figshare.com/articles/dataset/Harmonization_of_DMSP_and_VIIRS_nighttime_light_data_from_1992-2018_at_the_global_scale/9828827/5)
- Download all files from **2003 to 2018**
- Create folder **"Nighttime lights"** in "b_metadata"
- Insert files

---
 
## Execute the Code

Run the code file: **00_master_skript**

**Note in 10_merge_spei_afrogrid:**
The processing code (Code 10) includes a conditional block that is currently set to if(FALSE). This means the chunk processing step is skipped, and the script expects that the preprocessed merged dataset (conflict_afrogrid_allocated.csv) is already available in the a_microdata folder.
- When running the code, ensure that the merged dataset is already loaded in the a_microdata folder. If the file is not present, the code will terminate
- To Process from Scratch (Takes multiple hours!): Change the if(FALSE) statement (line 93)  to if(TRUE) to run the full processing pipeline.
