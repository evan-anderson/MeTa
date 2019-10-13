# Metabolic Tampering (MeTa) repository

Documentation and models from *Facilitating NMR Resonance Assignment with Metabolic Tampering*.
Authors: Danica Cui, Evan Anderson, Erik Zabala, George Lisi, J. Patrick Loria

In our upcoming publication *Facilitating NMR Resonance Assignment with Metabolic Tampering*, we describe a new method to aid in assignment of amino acids in NMR experiments. As a part of this publication, we describe implementation of a random forests classifier to classify amino acid identify in 2D <sup>15</sup>N HSQC experiments with varying, small amounts of enriched LB media. This repository serves as documentation for implementation and validation of this model, and also provides templates for implementation of this model by other users.


## File Summary

### Requirements and environment
`requirements.txt` lists the Python packages used in this analysis, and `environment.yml` is the conda environment file which I used for all of the following Jupyter Notebooks.

### Data processing, model selection, and validation
**meta_documentation.ipynb**: Jupyter Notebook describing data preprocessing, model selection, and model validation

**comparing_training_sets.ipynb**: Jupyter Notebook describing performance of the model with different train/test splits, including training on one protein (PTP1B) and testing on another (IGPS). 

### Notebooks for model implentation
**retrain_model.ipynb** Jupyter notebook serving as a template for training a random forest classifier model on your own data. `prepping sample data.ipynb` was used to create the place-holder data in this file. 

**all_unlabeled_model.ipynb** Jupyter notebook serving as a template for using the random forest classsifier trained on PTP1B and IGPS on your own unlabeled data.

### Data
This folder contains all of the data used in all of the jupyter notebooks in this repo. The datasets used to train the random forests classifier for our publication were:
`IGPS_8hr_0513.csv`
`PTP1B_8hr_0513.csv`

### Model
This folder contains the model which we trained `meta_documentation.ipynb` and which is used in `all_unlabeled_model.ipynb`. 

### Output
This folder contains the sample output data files from `retrain_model.ipynb` and `all_unlabeled_model.ipynb`, specifically with predicted labels for each peak. 



