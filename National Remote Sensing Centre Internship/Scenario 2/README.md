# Amazon Rainforest Deforestation Prediction

## Scenario

The Forest Department of Karnataka is working to protect endangered species in a tropical rainforest. They have access to a dataset of deforestation events and a shapefile of the rainforest boundaries. The goal is to identify areas of the rainforest that are most at risk of deforestation and focus conservation efforts on those areas. The solution involves developing a Python model and providing complete documentation.

## Dataset Description

This dataset contains historical satellite data about deforestation that occurred in the Amazon rainforest. The data includes deforestation rates in counties located in the Amazon rainforest. The dataset was obtained from the Brazilian National Institute for Space Research (INPE) and is available on Kaggle [here](https://www.kaggle.com/datasets/diegosilvadefrana/brazilian-deforestation-from-2000-to-2021).

### Counties.csv

| Column Name               | Type  | Description                                               |
| ------------------------- | ----- | --------------------------------------------------------- |
| Nome_Microrregião         | string| County Name                                               |
| Código Município Completo | int   | County Id where the first two numbers represent the state |

### data.csv

| Column Name   | Type   | Description                                            |
| --------------| ------ | ------------------------------------------------------ |
| ano           | int    | Year                                                   |
| id_municipio  | int    | County Id (same as in Counties.csv)                    |
| area          | int    | Total area measured                                    |
| desmatado     | float  | Total deforested area                                  |
| incremento    | float  | Incremental area measured after the previous measure   |
| floresta      | float  | Total forest area                                      |
| nuvem         | float  | Area covered by clouds                                 |
| nao_observado | float  | Non-measured area                                      |
| nao_floresta  | float  | Non-forest area                                        |
| hidrografia   | float  | Hydrographic area                                      |

### states.csv

| Column Name | Type | Description   |
| ------------| ---- | ------------- |
| estados_ido | int  | State id      |
| Estados     | int  | State name    |

## Required Visualizations

- Visualization 1:
- ![heatmap](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/175e3535-dc6c-4603-a855-531600a9af5d)

- Visualization 2:
- ![linechart](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/6c38df5b-1302-4c02-87a5-40929ec7c461)

- Visualization 3:
- ![multiplelinechart](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/6f1a9d35-2a0d-4ccf-b307-4644ce570b62)

- Visualization 4:
- ![predictionlinechart](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/fbd9c954-3d73-4969-8a31-d8672ec46557)


## Data Transformation
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/390c3896-233a-4a85-8fcb-d714909165da)


## Finding Counties with More Deforestation
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/1e8d9af2-6147-4d9e-a547-8b2c7633e1ef)


## Predicting Future Deforestation
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/b05ee21c-41df-47c4-89c4-ed171c33c0a3)

The chosen model is an ensemble model with three models: KNeighborsRegressor, SGDRegressor, and BaggingRegressor. This combination is expected to provide more precision according to the law of large numbers.
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/d68f249a-580f-44a0-ae56-b1bd3d5f1eea)

### Hyperparameters Tuning

![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/709c3198-975f-4c83-9d30-e4ad7fc66ec9)


### Evaluation Matrix
### Analysis and Performance of Regression Model
This present work combined three distinct datasets to analyze the deforestation rate in the Amazon region from the years 2000 to 2020.

After data preparation, the author used hyperparameters to calculate the best model with the aim of predicting the deforestation rate for the years 2022 and 2023.

As a method of error analysis, only the R² calculation was used.

We propose performing calculations for other error metrics to better evaluate the generated model.

R² The R² calculates the percentage of variance that could be predicted by the regression model, that is, how "close" the actual measurements are to our model.

The R² is inherently biased because, depending on the optimizer, it may use data correlation to erroneously increase the R² value. It can only be applied perfectly to models with only one input and does not respond well to overfitting.
### R square 
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/f51f53fe-e338-4195-ad99-365975b96bb9)
### Adjusted R Square
 ![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/8a2c636f-c908-4475-9fcb-77e393305be3)
### Mean Squared Error
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/afa5e62a-c1a2-49ea-8da8-25b166b98916)
### Mean Absolute Error
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/c8bcc9ed-ce3d-4f2a-9056-16adb22f45ab)
### Mean Absolute Percentage Error
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/cdfd7f50-c57f-4556-83b1-79c285cbd7f5)


## Conclusion

- Considering what was covered in class and the study of various types of metrics for error calculation in regression models, it is evident that determining the best formula for this calculation is a complex task.

- Among all the tested metrics, R² and Adjusted R² seem to have easily understandable values and indicate that the model has good predictive behavior.

- On the other hand, MSE, RMSE, and MAE presented values that are difficult to interpret, even though RMSE and MAE are in the same unit as the prediction. Their results suggest that the model is performing poorly.

- MAPE and RMSLE, which provide values in percentage terms, also indicate that the model is not well-trained, with MAPE showing a 107% error and RMSLE showing a 56% error.

- Based on the obtained data and the difficulty of understanding some of the algorithms for error evaluation, I maintain the author's opinion, suggesting R² or Adjusted R² as metrics for the model.

## GitHub Link

https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship.git

