Python  | Numpy | Pandas | Statsmodels | Sci-Kit Learn
--------|-----|-----|---------|------
[![PyPI](https://img.shields.io/badge/python-3.5-blue.svg)]() | [![PyPI version](https://badge.fury.io/py/numpy.svg)](https://badge.fury.io/py/numpy) | [![PyPI version](https://badge.fury.io/py/pandas.svg)](https://badge.fury.io/py/pandas) | [![PyPI version](https://badge.fury.io/py/statsmodels.svg)](https://badge.fury.io/py/statsmodels) |  [![PyPI version](https://badge.fury.io/py/scikit-learn.svg)](https://badge.fury.io/py/scikit-learn)

Slides live [here](https://docs.google.com/presentation/d/1wW8NGE5iaboHKFAvt0Dn0p0YvjA1_s8KumoZka54r3M/edit?usp=sharing).  **Clean notebooks coming soon**

# Southern California Reservoir Capacity Classifier

Classified drought levels at Summer's end (2000-2013) for reservoirs in Southern California using storage data and exogenous variables.

## Problem Statement

California’s recent drought has placed unprecedented demands on our freshwater resources, renewing enthusiasm for surface water infrastructure investments such as raising dams to capture more water in wet years. 

Reservoir improvements would need to consider the frequency and the extent to which these dams are depleted. 

My analysis looked at time series reservoir storage data around LA county to classify storage levels at summer’s end (Sept 1), given data about the rest of the year.

**Guiding Questions**
- Does climate serve as a valid predictor in classifying water availability?
- Can water availability be predicted using earlier monthly storage measurements?

## Data
- Data sourced from the Department of Water Resources  [California Data Exchange Center (CDEC)](http://cdec.water.ca.gov/cdecstation2/)
- Climate Data sourced from [Berkeley Earth](https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data)
  - Climate Monthly Average Temperature around Los Angeles (Average Temperature and Avg Error from 2000-2013)
- Additional information sourced from [Wikipedia](https://en.wikipedia.org/wiki/List_of_dams_and_reservoirs_in_California#cite_note-1):  Elevation of the dam, year completed, dam type (material),  heights (in feet and meters), capacity (in feet and meters.


## Analytical Approach

**Project Notes:**
- Adjusted storage measurements as proportions of the reservoir's capacity
- Make predictor features out of the storage af dataframe (1/1 - 6/1)
- Included climate data
  - Created dummy variables
    - Missing values (monthly storage measurements) were the means of the adjacent neighbors
- Make classes out of the storage af dataframe (9/1)
- Multiclass variables for four different reservoir conditions
- Train/Test Splits (climate data only goes to 2013…)
- Train set (2000 - 2010)
  - Test set (2011-2012)
  - Holdout set (2013)
- Classification model
- Feature engineering
  - Parameter optimization
  - Future work:
- Do I download more historical data (pre-2000?)
- Do I incorporate population data?
Visualization
- Flask & D3.js
  - https://www.dashingd3js.com/table-of-contents
  - The source: https://github.com/uwdata
  - What I really wanted:
	- http://bl.ocks.org/lokesh005/7640d9b562bf59b561d6
	- https://www.ucas.com/corporate/data-and-analysis/ucas-undergraduate-releases/equality-he-reports

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
More to come
```

## Limitations
- assumes business as usual water demand
- No natural disasters (wildfires and earthquakes)
- A static population size
- Unchanging urban, ag, and environmental uses
- Limited to reservoirs that had data available on CDEC
- Storage is the most complete predictor variable, with most reservoirs containing public data on storage
- Reservoirs that had recent data (2000-2017) were used in this analysis (as recent years give context to contemporary population size, consumption, water demand, etc).
- Some reservoirs had storage data dating back from the 80s to 2001
- Why CDEC stopped recording monthly storage data for some reservoirs, idk

## Future Work

Explain what next steps could involve


## Author

* [**Andrew Tom**](https://github.com/Atomahawk)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Problem & Visual Inspiration: http://ww2.kqed.org/lowdown/2015/09/21/now-that-summers-over-what-do-californias-reservoirs-look-like-a-real-time-visualization/
* etc
