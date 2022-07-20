Dataset preparation - used for generating the FINAL_DATASET.csv ( see the gdrive link in 02 generated datasets)
  extracts the streets of Vienna from osmnx ( type walk) and attaches to them through the use of geopandas.sindex features which were retrieved either from osmnx, austria opendata and other sources listed in the notebook.

Clustering streets - used for clustering and defining the street types. 

augmented_streets_ml_ - used for training the linear regression model for predicting the UHVI index from the collected features for every street.
