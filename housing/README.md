# Kaggle housing competition
- The goal of this project is to predict California housing prices given selected features (which may be missing/currupt)
- The loss function is log square loss

## Initial bench mark
- This is a very crude bench mark where a random forest of 500 shallow decision trees are used
- kaggle initial result a loss of 0.15323

## Data Analysis
- The initial data analysis is done in 
    - data_analysis_1,ipynb, data_analysis_2,ipynb 
- The first data processor is done in
    - data_processor.ipynb
    - filled NaN and zero heavy features by median
    - used 1hot encoding
    
## Final models
- housing_1.ipynb is a first model, mainy contributed by Krishan for data engineering
- housing_2.ipynb is the final model which achieved
    - top 15% in April 2019 with a log square loss of 0.11767
    - final result is in submit.csv
    - main features:
        - data engineering to include nonlinearity and ordered features by pearson correlation
        - used bagging with many simpler sklearn models followed by gradient boosting 
        - did not employ neural nets as this is a first test for basic machine learning algorithms