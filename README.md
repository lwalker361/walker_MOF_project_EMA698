# walker_MOF_project_EMA6938

Final project for EMA6938 - Machine learning applied to the pore-limiting diameter of metal-organic frameworks

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
(leave blank for now)
