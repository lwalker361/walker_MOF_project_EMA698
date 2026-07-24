# Walker_Project_EMA6938

Final project for EMA6938 - Machine learning prediction of the pore-limiting diameter of metal-organic frameworks

## The research question:
Can a random forest trained on geometric descriptors from MOSAEC-DB predict the pore limiting diameter of experimental MOFs with sufficient accuracy to rank candidates for gas separation screening?

## Instructions for obtaining the dataset used:
The full data set(s) are huge. We can download a partial dataset containing only the descriptors files. The files are small enough that they have been already been commited. If you needed to download fresh versions, follow the instructions below.

- Go to https://zenodo.org/records/15808197
- Files -> download descriptors.tar.gz
- Extract contents
- Find descriptors/descriptors/GEOM_mosaec-db.csv
- Copy the .csv and paste in /data

### Extra dataset information:
- The github repo for the origional database is here https://github.com/uowoolab/MOSAEC-DB/tree/main
- Their publication is here https://doi.org/10.1039/D4SC07438F
- Full citation: Marco Gibaldi, Anna Kapeliukha, Andrew White, Jun Luo, Robert Alex Mayo, Jake Burner, Tom K. Woo; MOSAEC-DB: a comprehensive database of experimental metal–organic frameworks with verified chemical accuracy suitable for molecular simulations. Chem. Sci. 2025; 16 (9): 4085–4100.
- The rest of the dataset is available for download here https://www.ccdc.cam.ac.uk/support-and-resources/downloads

## Setup instructions:
- Use environment.yml 
- No API keys are required

## Running the notebooks:
Run the following notebooks in this specific order (GEOM_mosaec-db.csv must be in /data):
1. `01_data_acquisition.ipynb`
2. `02_eda_featurization.ipynb`
3. `03_modeling.ipynb`
4. `04_results_visualization.ipynb`

## Brief summary of key results:

The random forest trained on a reduced feature set of geometric descriptors and grouped by unique MOF ID achieves a high R² and statistically significant predictive accuracy.

Model Performance Summary

R² Score:     0.8430 (± 0.0125)

MAE:  0.4397 Å (± 0.0094 Å)

RMSE: 0.7924 Å (± 0.0402 Å)

![Parity Plot](figures/parity_plot.png)

### Feature abbreviations key

cif = *Crystallographic Information File*

Unitcell_volume = *Unit Cell Volume*

Density = *Framework Mass Density*

ASA_A^2 = *Accessible Surface Area (in square Ångströms)*

ASA_m^2/cm^3 = *Volumetric Accessible Surface Area (in square meters per cubic centimeter)*

ASA_m^2/g = *Gravimetric Accessible Surface Area (in square meters per gram)*

NASA_A^2 = *Non-Accessible Surface Area (in square Ångströms)*

NASA_m^2/cm^3 = *Volumetric Non-Accessible Surface Area (in square meters per cubic centimeter)*

NASA_m^2/g = *Gravimetric Non-Accessible Surface Area (in square meters per gram)*

Largest included sphere = *Largest Included Sphere Diameter ($D_i$ / Maximum Cavity Diameter)*

Largest free sphere = *Largest Free Sphere Diameter ($D_f$ / Pore-Limiting Diameter)* TARGET PROPERTY

Largest included sphere along free sphere path = *Largest Included Sphere Diameter Along Free Sphere Path ($D_{if}$)*

AV_A^3 = *Accessible Volume (in cubic Ångströms)*

AV_Volume_fraction = *Accessible Volume Fraction (Void Fraction)*

AV_cm^3/g = *Gravimetric Accessible Volume (in cubic centimeters per gram)*

NAV_A^3 = *Non-Accessible Volume (in cubic Ångströms)*

NAV_Volume_fraction = *Non-Accessible Volume Fraction*

NAV_cm^3/g = *Gravimetric Non-Accessible Volume (in cubic centimeters per gram)*

POAV_A^3 = *Probe-Occupiable Accessible Volume (in cubic Ångströms)*

POAV_Volume_fraction = *Probe-Occupiable Accessible Volume Fraction*

POAV_cm^3/g = *Gravimetric Probe-Occupiable Accessible Volume (in cubic centimeters per gram)*

PONAV_A^3 = *Probe-Occupiable Non-Accessible Volume (in cubic Ångströms)*

PONAV_Volume_fraction = *Probe-Occupiable Non-Accessible Volume Fraction*

PONAV_cm^3/g = *Gravimetric Probe-Occupiable Non-Accessible Volume (in cubic centimeters per gram)*