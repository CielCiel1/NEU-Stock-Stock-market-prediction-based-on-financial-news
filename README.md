# NEU-Stock-Stock-market-prediction-based-on-financial-news
#### Table of contents
1. [Introduction](#introduction)
2. [Details](#details)
   - [Dataset](#Dataset)
   - [Proposedmodel](#Proposed_model)
3. [Results](#Results)
4. [Contact](#Contact)
<p align="center">
  <h1 align="center", id="introduction">NEU-STOCK</h1>
</p>

- In this study, we investigated and suggested a novel method for predicting stock values based on the effect of news articles. We chose 'Long short-term memory in conjunction with the 'Attention' mechanism after comparing and evaluating several alternative models. NEU-STOCK is tested using FPT's 1800 sample dataset and the website CafeF.vn.

## Details <a name="Details"></a>

### Dataset <a name="Dataset"></a>
- We developed two datasets, one to train the classification model, the other to train the stock price, prediction model.
`News classification dataset`. To be able to use PhoBERT to evaluate and categorize the news' impact, we built a dataset that included 1000 titles of financial articles taken from CafeF.vn and labeled them into three groups [negative, neutral, or positive] based on expert advice. The dataset includes 187 articles with a negative impact, 248 articles with no impact, and 565 articles positively.
`Stock price prediction dataset`. Our dataset contains FPT stock prices and related articles. To get the stock price, we collected 1800 closing prices of FPT stock from vn.investing.com for a period of seven years, between July 11, 2013, and September 24, 2020. Furthermore, we also crawled the news related to FPT Group from quality newspapers (e.g., CafeF.vn) in this period day by day. Then we classified the news's title by classification models and counted the number of positive, neutral, negative news each day. Finally, our dataset contains four main features as shown in the table below:

|   Feature    |               Meaning                    |
|:-----------: |:----------------------------------------:|
|   Price      |     The close price of FPT               |
|   Positive   |     The number of positive titles        |
|   Neutral    |     The number of neutral titles         |
|   Negative   |     The number of negative titles        |

### Proposed model  <a name="Proposed_model"></a>
- The method is built around two components: A stock news classification model and a prediction model based on `LSTM` and the `Attention` mechanism. The complete model's operating procedure is as the figure below: 
![] (https://github.com/CielCiel1/NEU-Stock-Stock-market-prediction-based-on-financial-news/blob/main/Image/ppmodel.PNG)

## Results <a name="Results"></a>
- The dataset is divided into two sets: training set with the first 1600 samples and testing set including the remaining 200 samples. We assessed LSTM and LSTM-Attention with news and without news performance based on the MAPE, RMSE, and R2 metrics.

|     |         LSTM            |             LSTM-Attention        |
|     |:-----------------------:|:---------------------------------:|
|     | With news |Without news |With news'NEU-Stock'|Without news  |
|:---:|:---------:|:-----------:|:------------------:|:------------:|
|MAPE |   1.386   |    1.370    |    1.338           |    1.734     |
|RMSE |  747.777  |   748.348   |   730.754          |   854.851    |
|R2   |   0.932   |    0.932    |    0.933           |    0.911     |  

The  prediction  of  NEU-Stock  on  the  test  set  is  illustrated  in below Figure.                               
![](https://github.com/CielCiel1/NEU-Stock-Stock-market-prediction-based-on-financial-news/blob/main/Image/model_att.png)
## Contact <a name="Contact"></a>
- Supervisor: [Tuan Nguyen](https://www.facebook.com/nttuan8)
- Team Members: [Trang Tran](https://www.facebook.com/cieltrantrang/),[Long Nguyen](https://www.facebook.com/lnn1208), [Tung Nguyen](https://www.facebook.com/gnutn0s), [Thao Nguyen](),  [Phuong Duong]() 
