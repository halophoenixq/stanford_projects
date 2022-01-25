# Archive of Stanford MS Statistics Projects

This repo holds the projects I worked on for my MS Statistics at Stanford.

1. Stock Price Predictions
Class: [STATS 202](https://stats-202.github.io/) - Data Mining and Analysis
Code (in R): [Google Colab](https://colab.research.google.com/drive/10Ze50f7lqaIhnqwnDOKastTpuRbXjEO7?usp=sharing), Downloaded Notebook

We were tasked with making a 9 day forecast at the 5-second granularity for 9 anonymized stock tickers. After exploring baseline and ARIMA models, we ultimately structured the problem as a direct forecasting problem and used the [forecast-ml package](https://github.com/nredell/forecastML) to train and make predictions. Note that we did not actually learn how to do time series analysis for this class, so we had to convert the problem into a structure we were familiar with.

2. Enhancing Short Term Air Quality Predictions with Location & Meteorological Data
Class: [STATS 207](https://stats207.github.io/) - Time Series Analysis
Code (in Python): [Google Colab](https://colab.research.google.com/drive/1KIKg49sdifofzCIjpVpQPysOMXAv9ILT?usp=sharing), Downloaded Notebook

We sought to build a 3 day ahead prediction for the air quality index of Santa Clara County. We approached the problem with increasingly complex models (ARMA, VARIMA, LSTM) and evaluated the performance increase with a sliding window cross-validation strategy. We specifically included AQI and meteorology data features from surrounding counties and improved performance when using relevant features.

Our presentation slides can be found [here](https://docs.google.com/presentation/d/1ceUaLOzDaqnKD3VWfMPAv-vJA9nDjUhnisoOHEsvEmo/edit?usp=sharing).

3. Impact of COVID Misinformation on Vaccination - A Reanalysis Identifying and Addressing Covariate Imabalances
Class: [STATS 209](https://explorecourses.stanford.edu/search?view=catalog&filter-coursestatus-Active=on&page=0&catalog=&q=STATS+209%3A+Introduction+to+Causal+Inference&collapse=) - Causal Inference
Code (in R): [Google Colab](https://colab.research.google.com/drive/1m-5hD2vt-CH9IzeQGlbHD6cQt5Qaih9b?usp=sharing), Downloaded Notebook

We reanalyzed a randomized controlled trial ([Original Paper](https://www.nature.com/articles/s41562-021-01056-1)[Original Github](https://github.com/sloomba/covid19-misinfo/)) that exposed participants to COVID misinformation and measured its impact on vaccination intent. We evaluated the study’s randomization and show that it is significantly imbalanced (p-value < 0.0001) using a Monte Carlo simulation of the Mahalanobis distance between Treatment and Control. We then reduced the bias of the estimates by applying matching estimators and performing regression adjustment using Lin’s Estimator. We also explored heterogeneous treatment effects and provide some intuitive insights.

4. Experiment - Can I Pay2Win for First Person Shooting Games?
Class: [STATS 263](https://artowen.su.domains/courses/363-1415/) - Design of Experiments
Code (in R): [Google Colab](https://colab.research.google.com/drive/1JXveQ5GIK52_TwRZ14CiS4XF6amgUXcJ?usp=sharing)

We were interested in understanding what factors can help improve an average person’s skills in shooting games and whether investing in better equipment (gaming mouse, high refresh rate monitor) really does make a significant impact on shooting skills. In addition, we wanted to see if a stimulant like coffee will be able to further enhance a player’s performance.

We structured our experiment as a combination of a strip-plot and stepped-wedge design. There were many logistic details that we considered during the design, ranging from how to parallelize the runs to whether we should serve hot or cold coffee.

This project focused on the design of the experiment and the data collection process. A proper experiment design helped drastically simplify what we needed to analyze.