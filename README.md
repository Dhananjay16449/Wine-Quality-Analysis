# Wine Quality Analysis and EDA

## Dataset Description:

There are two datasets that provides information on samples of red and white variants of the Portuduese "Vinho Verde" wine. Each sample of wine was rated for quality wine experts and examined with physicochemical tests. Data is originaly from [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/186/wine+quality).

## Columns Description:

1.  `fixed acidity`: concentration of non-volatile acids in wine, such as tartaric, malic, and citric acids.
2.  `volatile acidity`: amount of volatile acids in the wine, primarily acetic acid.
3.  `citric acid`: concentration of citric acid in the wine, which can add freshness and flavor.	
4.  `residual sugar`: amount of sugar remaining after fermentation stops.
5.  `chlorides`: amount of salt in the wine.	
6.  `free sulfur dioxide`: free form of SO2 in wine, which prevents microbial growth and oxidation. 
7.  `total sulfur dioxide`: total amount of SO2 in the wine(free + bound forms).	
8.  `density`: density of wine ,which is close to that of water depending on alcohol and sugar content.	
9.  `pH`: measure of wine's acidity or basicity on a scale from 0(very acidic) to 14(very basic).
10. `sulphates`: amount of sulphates in wine, which can contribute to sulfur dioxide gas levels.	
11. `alcohol`: The percentage of alcohol content in wine.	
12. `quality`: score between 0 and 10 rating the overall quality of the wine.

## EDA Questions:

- Q1: What chemical characteristics are most important in predicting the quality of wine?
- Q2: Is a certain type of wine(red or white) associated with higher quality?
- Q3: Do wine with higher alcohol content receive better ratings?
- Q4: Do sweeter wines(more residual sugar) receive better ratings?
- Q5: What level of acidity(pH) is associated with the highest quality?

## Data Wrangling:

Data wrangling is the process of cleaning, transforming, and preparing data for analysis. 
Our data can be found on `wineQualityReds.csv` and `wineQualityWhites.csv` files provided on this repository, downloaded from [Kaggle](https://www.kaggle.com/datasets/danielpanizzo/wine-quality) and originaly from [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/186/wine+quality).

## Data Cleaning:

**Exploration Summary**

- Red wine dataframe consists of 1599 records and 13 attributes, while white wine dataframe consists of 4898 records and same attributes.
- Both dataframes has no NaNs nor duplicated values.
- We would combine both dataframes and append a new categorical column to indicate the wine color for better analysis.
- Columns data types are consistant.
- `Unnamed: 0` column would be dropped.

We endded up with 13 columns and 6497 rows for our data to begin the analysis with a new csv file containing our full data is saved in `wine.csv`.

## Data Visualization:

Using `Matplotlib` and `Seaborn`, we made several meaningful visuals and charts to help us in fgaining informative insights regarding any correlation between attributes in our dataset, that'll be discussed in the next section.

## Conclusion:

These are derived conclusions after completing our data visualisation phase.

**Q1: What chemical characteristics are most important in predicting the quality of wine?**

- The vast majority of the wine has a `quality` score of 6, while less numbers has a `quality`
score of 9.
- Using correlation plot, we can easily see if certain attributes are correleated more strongly to wine quality than some others.
  - Strong correlated attributes:
    - `alcohol` and `quality`, and it's clear that this is the highest relation that affets wine quality.
  - Weak correlated attributes(do not depend on each other):
    - `density` and `alcohol`.
    - `free.sulphur.dioxide` and `citric.acid` has almost no correlation with quality.
  - `density` has strong positive correlation with `residual.sugar` and strong negative correlation with `alcohol`.


**Q2: Is a certain type of wine (red or white) associated with higher quality?**

- There is noticable deviation between white and red wine counts.
- We can notice that white wine forms the majority of our dataset, with 85.7% of the data points belonging to this category. 
- Most of the white wine has a quality score of 6, while most of the red wine has a quality score of 5.
- The average quality score of red and white wine are very close.
- The mean quality score of white wine is higher than that of red wine.

**Q3: Do wines with higher alcoholic content receive better ratings?**

- We have the hghest alcohol content at 14.9.
- Mean alcoholic content is around 10.4.
- Most of our dataset that has a quality score of 6 appears to have relatively low alcoholic content, but it still above the mean.
- High alcoholic content only appears in our dataset with high quality wine.

**Q4: Do sweeter wines (more residual sugar) receive better ratings?**

- We can see that the highest sugar content is tied to a quality of 5, while lower the sugar content appears to have respectively higher quality.

**Q5: What level of acidity (pH) is associated with the highest quality?**

- Most of the wine in our dataset has high acidic level
- It looks clear that all four acidic level has close average quality score, but low acidic level has the highest quality score in dataset.


## Built with:
- Visual Studio Code
- Python3
- Pandas
- Numpy
- Matplotlib
- Seaborn










