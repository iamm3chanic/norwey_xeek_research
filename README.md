# Project for investigation of Norway wells dataset
Stratigraphic interpretation: applying ML algorithms in formation tops prediction problem.

Here is my [paper](https://onepetro.org/SPEADIP/proceedings-abstract/23ADIP/23ADIP/D011S022R004/534299?redirectedFrom=PDF) with some Methodology explanation. 

## Data overview

![Data presence over dataset](https://github.com/iamm3chanic/norwey_xeek_research/blob/master/results/figures/data_presence.png)

![Lithology map](https://github.com/iamm3chanic/norwey_xeek_research/blob/master/results/figures/map_overview_lithology.png)

![Lithology vs formation distribution](https://github.com/iamm3chanic/norwey_xeek_research/blob/master/results/figures/lithology_formation_presence.png)



## Structure

Project has 5 stages:

1. Data preparation
    1. Choosing region with closely located wells
    2. Choosing and scaling needed features
    3. Scaling numeric features by well
    4. Saving valid formation orders
    5. For each well find 5 most similar wells by:
        1. Order similarity
        2. Coordinates
    6. Store numbers of similar wells
2. Building models
    1. Feature selection
    2. Changepoint models
   3. Optuna trials: hyperparameter updates
   4. DTW similarity for formation labels
   5. Tsfresh feature extraction + filtering
   6. CatBoost/XGBoost/RF/KNN for formation labels
3. Testing models
    1. Changepoint models
   2. Classification (labeling) models
   3. Store results 
4. Counting metrics
    1. Simple order intersection 
    2. Precision, Recall, Randindex, Hausdorf distance
    3. Custom SIOU metrics (A. Lipko)
    4. Draw distribution of metrics based on wells/sets
    5. Find interwell correlation
   6. Table of metrics
5. Drawing wells
    1. Source + prediction + metrics
    2. Maps
    3. Graphs of similarity
    3. Heatmaps

