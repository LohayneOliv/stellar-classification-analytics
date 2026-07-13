# Astronomic Census & Spectral Classification (Google Sheets)

Developing a collaborative spreadsheet-based ecosystem to automate celestial body screening and stellar lifecycle modeling using the ESA Hipparcos Catalog.

## 📌 Project Overview
* **The Business Problem**: Educational institutions and small astronomy laboratories lack expensive, proprietary software for rapid observational data screening. There was a critical need to centralize raw telescope data and build an accessible, cost-effective, and fully automated analytics system to classify stars by temperature.
* **The Dataset**: A subset of the official Hipparcos Catalog (ESA) containing unique star IDs, Right Ascension/Declination coordinates, Absolute Magnitude, and Effective Temperature measurements (K).
* **Core Tools**: Google Sheets, Google Apps Script, Advanced Formulas.

## 🛠️ Data Engineering Process

1. **Data Cleaning**: Ingested and cleaned raw telemetry datasets by executing deduplication protocols in the `Dados_Brutos` tab.
2. **Feature Engineering**: Built real-time calculated columns for spectral class indexing using nested conditional logic and array constraints to keep processing lightweight.
3. **Data Aggregation**: Aggregated and summarized multi-variable data points using optimized Pivot Tables mapped directly to the interactive dashboard view.

### Key Logic Applied (Formula):
```excel
=ARRAYFORMULA(IF(A2:A="", "", IFS(C2:C>=30000, "Classe O (Azul)", C2:C>=10000, "Classe B", C2:C>=7500, "Classe A", C2:C>=6000, "Classe F", C2:C>=5200, "Classe G (Tipo Sol)", C2:C>=3700, "Classe K", TRUE, "Classe M")))
```

## 📊 Analytical Results & Value
* **Automação Total**: Manual stellar categorization time was reduced to zero through the automated logical matrix execution.
* **Demographic Insight**: The analytical dashboard visually proved that low-mass cold stars (**Class M**) dominate 76% of the regional volumetric sample, optimizing the trajectory of academic research allocation.

## 🔗 Live Project Access
* [Access the Interactive Google Sheet Dashboard](https://docs.google.com/spreadsheets/d/1YV2kypzsYVjMi_nU8yOz6ejjbWhB-EdNuqUs1RnVruQ/edit?usp=sharing)
# stellar-classification-analytics
Stellar classification and astronomic census dashboard built with Google Sheets
