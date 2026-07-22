walker_MOF_project_EMA6938
Final project for EMA6938 - Machine Learning Applied to the Pore-limiting Diameter of Metal Organic Frameworks

The research question:
  Can a random forest trained on geometric descriptors from MOSAEC-DB predict the pore limiting diameter of experimental MOFs with sufficient accuracy to rank candidates for gas separation screening?

Instructions for obtaining the dataset used:
  The full data set(s) are huge. We can download a partial dataset containing only the descriptors files.
  Go to https://zenodo.org/records/15808197
  Files -> download descriptors.tar.gz
  Extract contents
  Find descriptors/descriptors/GEOM_mosaec-db.csv
  Copy the .csv and paste in /data 

  Extra dataset information:
    The github repo for the origional database is here https://github.com/uowoolab/MOSAEC-DB/tree/main
    Their publication is here https://doi.org/10.1039/D4SC07438F
    The rest of the dataset is available for download here https://www.ccdc.cam.ac.uk/support-and-resources/downloads

Setup instructions:
  No environment is required
  No API keys are required

Running the notebooks:
  Run the following notebooks in this specific order after GEOM_mosaec-db.csv has been copied to /data
    01_data_acquisition.ipynb
    02_eda_featurization.ipynb
    03_modeling.ipynb
    04_results_visualization.ipynb

Brief summary of key results:
  (leave blank for now)
