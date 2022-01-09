# Pair-Trading-with-DDDQN

## Description
Optimize pair trading performance with reinforcement learning algorithm (DDQN and DDDQN).

## Structure
- data
  - *.csv: daily stock price downloaded from [Yahoo Finance](https://finance.yahoo.com/)
  - get_data.ipynb: download data from [Yahoo Finance](https://finance.yahoo.com/)
  - process.ipynb: explore cointegration relationship of two stocks
  - select_pair.ipynb: use distance approach and cointegration approach to select appropriate stock pair for pair trading
- pre-train
  - main.ipynb: create a base model composed of convolution layers, train the model on specific stock pair to predict the trend of spread. The well-trained base model will later be used in RL models train with DDQN and DDDQN.
- train
  - double_dqn.ipynb: use double dqn algorithm to train RL agent in pair trading
  - dueling_double_dqn.ipynb: use dueling double dqn algorithm to train RL agent in pair trading
  - pair trading environment is defined in these two files
- test
  - baseline_testing.ipynb: test the performance of baseline approach (rule-based)
  - nn_testing.ipynb: test the performance of RL agent trained by DDQN and DDDQN
  - xgboost_testing.ipynb: test the performance of XGBoost algorithm
## Run
All scripts are written in jupyter notebook, you can run it on [colab](https://colab.research.google.com/?utm_source=scs-index) or [kaggle](https://www.kaggle.com/). 

### Caution
- Make sure the the path of dataset is correct in scripts.</br>
- The version of TensorFlow >= 2.0

## Resource

You may use these resources to uderstand this project.

- Presentation ([Slide](https://github.com/johnnyhwu/Pair-Trading-with-RL-DDDQN/blob/main/slide.pdf), [Video](https://youtu.be/n0lTbl0Thq0))
- [Report](https://github.com/johnnyhwu/Pair-Trading-with-RL-DDDQN/blob/main/report.pdf)
