# Cookiecutter Data Science

_A logical, reasonably standardized, but flexible project structure for doing and sharing data science work._

### Standard Naming Convention

Files should be named according to the person who is creating them, version numbers, and the purpose. For example:
* notebooks/ak-1.2-DataPreprocessing.py
* data/interim/ak-1.2-DataPreprocessing.csv
* logs/ak-1.2-DataPreprocessing/GENERATED_FILES

Your initials (preferably first two), the notebook number (in chronological order of creation) and version number (incremented any time you make changes that would effect the output, and the type of file.

#### Common file names
* DataPreprocessing - manipulating the raw data files into standard Pandas Dataframe form
* DataExploration - for looking at the contents of the data, usually raw but could be other
* ModelX - running a particular model
* ParameterTuning - sweeping across hyperparameters
* Scratch - personal playground, not expected to be production ready at any point


#### [Project homepage](http://drivendata.github.io/cookiecutter-data-science/)

### Requirements to use the cookiecutter template:
-----------
 - Python 2.7 or 3
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```


### To start a new project, run:
------------

    cookiecutter https://github.com/AmiiThinks/cookiecutter-data-science


[![asciicast](https://asciinema.org/a/9bgl5qh17wlop4xyxu9n9wr02.png)](https://asciinema.org/a/9bgl5qh17wlop4xyxu9n9wr02)


### The resulting directory structure
------------

The directory structure of your new project looks like this: 

```
├── LICENSE
├── Makefile           <- Makefile with commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│       └── README.md  <- Link or instructions on acquiring the data
│   ├── interim        <- Intermediate data that has been transformed, use standard naming convention.
│   ├── processed      <- The final, canonical data sets for modeling, snc refers to relevant notebooks.
│   └── raw            <- The original, immutable data dump.
│       └── README.md  <- Link or instructions on acquiring the data
│
├── docs               <- A default Sphinx project; see sphinx-doc.org for details
│
├── logs               <- Stores details of experiments, learning curves from custom tools
│   └── ID-#-nb        <- Directory referencing the notebook or commit used to create logs.
|
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is the creator's initials,
│                         a number (for ordering), and a CamelCase description, e.g.
│                         `ak-1.0-DataPreprocessing.ipynb`.
│
├── references         <- Relevant papers, Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── src                <- Source code for use in this project, the ultimate deliverable
│   ├── __init__.py    <- Makes src a Python module
│   │
│   ├── data           <- Scripts to download or generate data
│   │   └── make_dataset.py
│   │
│   ├── features       <- Scripts to turn raw data into features for modeling
│   │   └── build_features.py
│   │
│   ├── models         <- Scripts to train models and then use trained models to make
│   │   │                 predictions
│   │   ├── predict_model.py
│   │   └── train_model.py
│   │
│   └── visualization  <- Scripts to create exploratory and results oriented visualizations
│       └── visualize.py
│
└── tox.ini            <- tox file with settings for running tox; see tox.testrun.org
```

## Contributing

We welcome contributions! [See the docs for guidelines](https://drivendata.github.io/cookiecutter-data-science/#contributing).

### Installing development requirements
------------

    pip install -r requirements.txt

### Running the tests
------------

    py.test tests
