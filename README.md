# Machine Learning 2021 Project

This repository introduces three machine learning algorithms as well as the Analysis of Variance (ANOVA) analysis technique and their implementations in Python. The content is geared towards undergraduate level readers, or folks fairly new to machine learning, and doesn't require an advanced understanding of mathematics or statistics. The content does assume some familiarity with Python and coding practices though, as it does explain how to use these algorithms but does not go into detail other areas such as how to plot the graphs.

The main Python libraries used in this repository are Scikit-Learn, Scipy.Stats and Statsmodels. You can find a full list of required libraries in the requirements.txt file, and further details on installation below.

This repository is Brian Doheny's submission for the 2021 Machine Learning module at Galway-Mayo Institute of Technology (GMIT).

## Repository Contents

**scikit_learn.ipynb:** A Jupyter Notebook introducing the Scikit-Learn Python library for machine learning, and three of the algorithms available in Scikit-Learn (Support Vector Classifiers, Random Forest Classifiers and KMeans Clustering). All of the data required for this notebook is generated within the notebook itself via Scikit-Learn.  The libraries required to run this notebook are contained within requirements.txt. 

You can also access this notebook via NBViewer:

[![nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.org/github/OtherBrian/machine-learning/blob/main/scikit_learn.ipynb)

Or you can view an interactive version via Binder:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/OtherBrian/machine-learning/49d445dafa1b5e5217dee9183dbbc5625e66f4cf)

**scipy_stats.ipynb:** A Jupyter Notebook introducing the Scipy.Stats Python library for statistical analysis, as well as an introduction to hypothesis testing and ANOVA. The datasets used for this notebook are contained within the datasets folder, and the libraries required to run this notebook are contained within requirements.txt.

You can also access this notebook via NBViewer:

[![nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.org/github/OtherBrian/machine-learning/blob/main/scipy_stats.ipynb)

Or you can view an interactive version via Binder:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/OtherBrian/machine-learning/49d445dafa1b5e5217dee9183dbbc5625e66f4cf)

**Datasets folder:** Contains three datasets which are used in the scipy_stats.ipynb to demonstrate ANOVA. The three datasets are:
* **Diet dataset (diet.csv)** - This dataset was sourced from [Sheffield University](https://www.sheffield.ac.uk/mash/statistics/datasets) and is a toy dataset containing 78 observations across 3 variations of diet. This dataset is already very tidy and ideal for ANOVA, and so is used for a general overview.
* **Students dataset (students.csv)** - This dataset was sourced from [Freie Universität Berlin](https://www.geo.fu-berlin.de/en/v/soga/Basics-of-statistics/ANOVA/One-way-ANOVA-Hypothesis-Test/index.html) and contains 8239 observations of student salaries alongside key variables from their time in college. This dataset requires some cleaning (as is done in the notebook) and is used for a more thorough, and more realistic introduction to using ANOVA.
* **Irish Weather dataset (irish_weather.csv)** - This dataset was sourced from [Kaggle](https://www.kaggle.com/conorrot/irish-weather-hourly-data) and contains the hourly weather measurements across various locations in Ireland. The csv contained in this depository has been trimmed massively, and now only contains measurements from Athenry. This dataset is only used as an example of the limitations of the Shapiro-Wilk test (introduced in the scipy-stats.ipynb) and shows an alternative test.

**Images folder:** Contains illustrations that are used throughout the two Jupyter Notebooks. All illustrations were created myself via [Excalidraw](https://excalidraw.com/). Each illustration is included as a png file for use, and the original excalidraw files are contained within the excalidraw_files folder, and these can be opened in Excalidraw and edited or updated.

**requirements.txt:** The Python libraries required to run both of the above mentioned Jupyter Notebooks. This can be used to set up a virtual environment to run the notebooks in. You can find more details on this below.

**README.md:** You are currently reading this file. It provides an overview of this repository and its contents.


## How to use this repository

### Installing Python and required libraries

In order to run the Jupyter Notebooks in this repository, you will require Python to be installed on the machine. These were created with Python version 3.8.5.

You can install Python via [Python.org](https://www.python.org/downloads/).

As for the libraries that are required, you will need:
* numpy
* pandas
* matplotlib.pyplot
* seaborn
* sklearn
* scipy.stats
* pingouin

You can install these individually via the command line by typing ([as outlined here](https://datatofish.com/install-package-python-using-pip/)):

```pip install [package name]```

Alternatively you can install all of these packages via the requirements.txt file by typing the following into the command line:

```pip install -r requirements.txt```

Finally, if you intend to use Python for data analysis in future, you may consider installing Anaconda. This includes many of the most popular libraries for data science and analytics in one handy package. [You can install Anaconda from here](https://www.anaconda.com/products/individual). 

**Note: The Pinguoin and Scikit-Posthocs libraries are not included in Anaconda at present, and so will need to be installed via one of the two above methods regardless. These libraries are used to show the Games-Howell Post-Hoc Multiple Comparisons test and Dunn's test in scipy_stats.ipynb.**

### Cloning the repository and running it on a local machine

You can clone the repository to your local device by clicking the green "Code" button found in the top right section of the screen. Here you'll be given multiple options on how you wish to clone the repository. You can find details on each of these options in [GitHub's documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository).

![Code button in Github Repository](https://screenshot.click/29_02-nn6ea-s7bhv.jpg)

Once the repository is cloned, you can navigate to the folder it was saved to via your command line by using the "cd" command (Change Directory). For example:

```cd ../college/machine-learning```

Once in the repository, open a Jupyter Notebook session by typing the following into your command line:

```jupyter notebook```

This will launch a Jupyter Notebook environment in your browser. From here you can open all of the files within the repository, and it should look something like this:

![Jupyter Notebook folders](https://screenshot.click/29_18-xj4g2-zo1tz.jpg)

You can then open the ipynb files by double clicking them. When you first open the notebooks, you should find all of the code cells have run and are thus showing their output and results. If you wish to clear the output of the code cells, click "Kernel" in the menu and select "Restart & Clear Output".

![Reset kernel and clear output](https://screenshot.click/29_21-kfa64-lzcaw.jpg)

You can then choose to either "Run" all of the cells by going into the "Cell" menu and selecting "Run All". This will run the code in each cell and thus generate output. Alternatively you can go through the notebook cell by cell and run their contents in turn by selecting the cell and pressing Shift+Enter on your keyboard. 

**Note: The code cells should be run in order, as later cells rely on code from prior cells. Running the cells out of order will lead to errors. If you are encountering such errors and can't work out which cell is causing it, consider going to the "Kernel" menu and selecting "Restart Kernel and Run All".**

[You can find more information on how to use Jupyter Notebooks here](https://www.dataquest.io/blog/jupyter-notebook-tutorial/).

### Viewing the notebooks via NBViewer

Both notebooks are also available via NBViewer. This renders the notebook so that it can be accessed via a URL, although the cells cannot be interacted with like in a live Jupyter Notebook. You can find the NBViewer links via the buttons at the top of the two notebooks, or in the Repository Contents section above.

### Viewing the notebooks via Binder

Similar to NBViewer, Binder allows us to host our Jupyter Notebooks online while allowing users to still interact with the cells. You can find the URLs for the two notebooks in Binder via the buttons at the top of the two notebooks or in the Repository Contents section above.