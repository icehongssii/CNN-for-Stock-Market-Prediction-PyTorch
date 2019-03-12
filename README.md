# How to use
1. checkout Requirements from the below

2. get into the source dir
```
cd source
```
3. execute cnn.py with data samples
```
python cnn.py ../data
```
4. if you want to use more data, use the data from ```data/original```... instead of using ```data/sample```..
--------------------------------------------------------
# Requirements

This code is based on ```python3.5.2 ``` and ```anaconda4.2.0```.     
highly recommend to use ```virtualenv``` such as virtualenv and conda

e.g)if you installed anaconda, use conda to create virtualenv and activate it.
```
conda create -n virtualenvname python=3.5.2
source activate virtualenvname
```

then, install the required packages to execute the code
```
pip install -r requirements.txt
```
--------------------------------------------------------
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

---------------------------------------------
