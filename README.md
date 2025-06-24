# Master Thesis: Land grabs and social conflict in Africa  
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

*From now on, all files have to be loaded into the folder "b_metadata".*

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



## 5. Nighttime Lights

[Nighttime Lights Dataset on Figshare](https://figshare.com/articles/dataset/Harmonization_of_DMSP_and_VIIRS_nighttime_light_data_from_1992-2018_at_the_global_scale/9828827/5)
- Download all files from **2003 to 2018**
- Create folder **"Nighttime lights"** in "b_metadata"
- Insert files

---

## 6. Population

[Nighttime Lights Dataset on Figshare](https://hub.worldpop.org/geodata/summary?id=139)
- Download entire Dataset
- Create folder **"population"** in "b_metadata"
- Insert files
  
---

 ## 7. African Boundary

[African Boundaries on opendatasoft](https://public.opendatasoft.com/explore/dataset/world-administrative-boundaries/export/?location=2,14.26438,51.32813&basemap=jawg.light)
- Download GeoJSON file
- Rename to "Africa_countries.geojson" in "b_metadata"

---

 ## 8. Insert intermediate Data
**Note in 8_merge_spei_afrogrid:**
The processing code (Code 8) includes a conditional block that is currently set to if(FALSE). This means the chunk processing step is skipped, and the script expects that the preprocessed merged dataset (spei_afrogrid_allocated.csv) is already available in the a_microdata folder.
- When running the code, ensure that the merged dataset is already loaded in the a_microdata folder. If the file is not present, the code will terminate
- To Process from Scratch (Takes multiple hours!): Change the if(FALSE) statement (line 97)  to if(TRUE) to run the full processing pipeline.

## Execute the Code

Run the code file: **00_master_skript**
