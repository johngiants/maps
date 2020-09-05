maps
==============================

This project went through two phases:
    - interactive geotracking of my Google Maps data
    - modern visualizations of countries I visited with the purpose of creating a "map room" in my apartment
    
The final output looks like this:

![Desk 1](https://github.com/johngiants/maps/tree/master/reports/final/desk_map_1.jpg)

![Desk 2](reports/final/desk_map_2.jpg)

How to:
==============================
Disclaimer: Unlike a real data science project, most of the features of this project are not located directly in the Makefile.

To run this project, first create a conda environment from the yml file "environment.yml" using the usual conda cmd.

```
conda env create --file envname.yml
```
Use the Makefile to download the shapefile data required to plot the map. The cmd is the following: 

```
make download_data
```

For the rest of the project, simply navigate the jupyter notebooks. An automated solution directly in the Makefile is not wished as it is not suitable for this specific project. Each map requires small adjustements, which are mostly based on visualization i.e. the way it looks in the notebook or because of software requirements when trying to print the maps. 


    
Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`. Please note that here the only available cmd is `make download_data`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources i.e. shape files.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump. Here my gmaps location data.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting. Here the final maps to be printed.
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
