# Your review

Selected paper: Improving Subseasonal Forecasting in the Western U.S. with Machine Learning

### Summary

In order to improve the accuracy of the long-term forecasts of temperature and precipitation for better water management in the western U.S., the U.S Bureau of Reclamation and the NOAA launched the Subseasonal Climate Forecast Rodeo aimed to skilfully predict temperature and precipitation 2-4 weeks and 4-6 weeks in advance for better resource allocation. This paper released their own subseasonal machine learning (MI) system, to help improve accuracy and to advance the state of art in subseasonal forecasting. Their system is an ensemble of 2 nonlinear regression models: the MultiLLR model which introduces candidate regressors from each data source in the SubseasonalRodeo dataset and then prunes irrelevant predictors using multitask backward stepwise criterion; and the AutoKNN model which uses only historical measurements of the target variable (temperature/ precipitation) and introduces multitask nearest neighbour features into a weighted local linear regression. Their results show that each model alone is significantly more accurate than the debiased operational U.S. Climate Forecasting System (CFSv2), and an ensemble of their regression models improves debiased CFSv2 skill by 40-50% for temperature and 129-169% for precipitation over year 2011-2018.

### Strengths

This paper contributed to the knowledge gap that even though ML approaches have been successfully applied to both short-term (<2 weeks) weather forecasting and long term (months to years) climate prediction, mid-term subseasonal outlooks (which depend on both local weather and global climate variables) still lack skilful forecasts. They therefore released a new SubseasonalRodeo dataset suitable for training and benchmarking subseasonal forecasts, and introduced a simple ensembling procedure that provably improves average skill whenever average skill is positive.

### Weaknesses and limitations

This paper evaluated their model forecasts over the Rodeo contest period, and for each target date in the contest period, Rodeo organizers provided the skills of 2 baseline models (deviased CFSv2 & damped persistence). This paper reconstructed a deviased CFSv2 outside the contest period, but unable to recreate the damped persistence model as no exact description was provided. Also, while the official contest CFSv2 baseline averages the forecasts of 4 model initializations, the CFSv2 Operational Forecast dataset only provided the forecasts of 1 model initialization, thus the reconstruction of this paper does not precisely match the contest baseline, but it provides a similarly competitive benchmark.

### Implications

This paper exposed the ML community to an important problem ripe for ML development: improving subseasonal forecasting for water and fire management, and demonstrated that ML tools can lead to significant improvements in subseasonal forecasting skill. This paper stimulates future development and evaluation of additional subseasonal forecasting approaches with the release of their user-friendly Python Pandas SubseasonalRodeo dataset.

### 

