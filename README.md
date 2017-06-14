Python  | Numpy | Pandas | Statsmodels | Sci-Kit Learn
--------|-----|-----|---------|------
[![PyPI](https://img.shields.io/badge/python-3.5-blue.svg)]() | [![PyPI version](https://badge.fury.io/py/numpy.svg)](https://badge.fury.io/py/numpy) | [![PyPI version](https://badge.fury.io/py/pandas.svg)](https://badge.fury.io/py/pandas) | [![PyPI version](https://badge.fury.io/py/statsmodels.svg)](https://badge.fury.io/py/statsmodels) |  [![PyPI version](https://badge.fury.io/py/scikit-learn.svg)](https://badge.fury.io/py/scikit-learn)

Repo update in progress!  Rough readme lives [here](https://docs.google.com/document/d/1gRqm81WZ4JwHMFXvFq-dKE6lQohWEMX9ViEZSQJeJpY/edit#)

Slides live [here](https://docs.google.com/presentation/d/1wW8NGE5iaboHKFAvt0Dn0p0YvjA1_s8KumoZka54r3M/edit?usp=sharing).  **Code coming soon**

# Southern California Reservoir Capacity Classifier

Classified drought levels at Summer's end (2000-2013) for reservoirs in Southern California using storage data and exogenous variables.

## Problem Statement

California’s recent drought has placed unprecedented demands on our freshwater resources, renewing enthusiasm for surface water infrastructure investments such as raising dams to capture more water in wet years. 

Reservoir improvements would need to consider the frequency and the extent to which these dams are depleted. 

My analysis looked at time series reservoir storage data around LA county to classify storage levels at summer’s end (Sept 1), given data about the rest of the year.

## Data
- Data sourced from the Department of Water Resources  [California Data Exchange Center (CDEC)](http://cdec.water.ca.gov/cdecstation2/)
- Climate Data sourced from [Berkeley Earth](https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data)
  - Climate Monthly Average Temperature around Los Angeles (Average Temperature and Avg Error from 2000-2013)
- Additional information sourced from [Wikipedia](https://en.wikipedia.org/wiki/List_of_dams_and_reservoirs_in_California#cite_note-1):  Elevation of the dam, year completed, dam type (material),  heights (in feet and meters), capacity (in feet and meters.


## Analytical Approach

Will better explain the questions guiding analyses and a summary of the methods involved

## Tool Stack

- AWS t2.micro EC2 instance with a PostgreSQL database
- Jupyter notebook
- Python 3.5
- Pandas, Matplotlib, Seaborn
- Sci-kit Learn
- Plotly

Might include step by step series of examples that tell you have to get a development env running

## Visuals [In Development]
- https://plot.ly/~atomahawk/48/storage-for-major-reservoirs-around-los-angeles-county/ 
- https://plot.ly/~atomahawk/50/reservoir-storage-capacities-in-2001/


## Conclusions
More to come.  Will explain insights gleaned, model evaluation, or patterns in visualization.

Best Performer: Random Forest Classifier
- Max Depth: 3
- Number of estimators = 3


```
Give an example
```

## Future Work

Explain what next steps could involve


## Author

* [**Andrew Tom**](https://github.com/Atomahawk)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Problem & Visual Inspiration: http://ww2.kqed.org/lowdown/2015/09/21/now-that-summers-over-what-do-californias-reservoirs-look-like-a-real-time-visualization/
* etc
