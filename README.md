# Requirements
`conda env create -f environment.yml`    
`pip install https://github.com/matplotlib/mpl_finance/archive/master.zip`    
[mpl_finace was deprecated](https://stackoverflow.com/questions/42373104/since-matplotlib-finance-has-been-deprecated-how-can-i-use-the-new-mpl-finance)    
Possibly it will be updated by using docker 

# How to run
go to `source` dir then run below code   
1. cnn.py version
`python cnn.py ../data`
2. cnn4matrix.py version
`python cnn4matrix.py matrixdata`


# Options
if you attempt to make new label and new matrix ..     
`python main-gen.py -m ohlcvdata 10 matrixdata`

# Can Machine Reads Like Analysts Do?

- Train a CNN to read candlestick graphs, predicting future trend.

- Training & testing Dataset from [Huge Stock Market Dataset-Full Historical Daily Price + Volume Data For All U.S. Stocks & ETFs](https://www.kaggle.com/borismarjanovic/price-volume-data-for-all-us-stocks-etfs).

- Pytorch implementation

## Two Approaches
### Approach 1
- `cnn4matrix.py`

- Apply convolution on data matrices directly.

Input: (5\*n) matrices -> (Open,High,Low,Close,Volume)\*(d1,d2,...,dn)

Output: classification result

### Approach 2
- `cnn.py`

- Generate candlestick graphs first.
![sample](https://github.com/hardyqr/CNN-for-Stock-Market-Prediction/blob/master/screen_shots_logs/sample.png)

Input: candlestick graphs

Output: classification result


## Current results

11 layers + residual block
![prediction](https://github.com/hardyqr/Deep-Learning-for-Stock-Market-Prediction/blob/master/screen_shots_logs/sota/acc+loss.png)
