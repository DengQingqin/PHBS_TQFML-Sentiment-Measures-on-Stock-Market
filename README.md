## Sentiment Factors on Stock Market 
Team Member: Deng Qingqin (1701213019)
Dataset Source: from Wind
### Motivation and Goal
Market sentiment refers to the investor’s belief based on the expected future cash flow and risk of the asset. For different assets, different people have different "beliefs" that we call "sentiment”. When investors' sentiments tend to be consistent under the influence of social interaction mechanisms, such "sentiments" may affect asset pricing and investment returns.
Through the research and analysis of sentiment indicators, I choose 8 indicators to construct a mood index, and I would like to apply some machine learning methods to see whether it would work efficiently on predicting the change of HS300 Index change.
### Data Description
![alt text](https://github.com/DengQingqin/PHBS_TQFML-Sentiment-Measures-on-Stock-Market/blob/master/1.png "Logo Title Text 1")
According some research reports and papers, I choose 8 sentiment factors.
The data ranges from 2010 to 2018.
The data includes 8 sentiment factors (independent variables):
1.	A-Share investor growth
2.	A-Share turnover rate
3.	ETF net redemption rate
4.	Financing balance growth
5.	HS300 stock index futures monthly premium
6.	50ETF PCR (put call ratio)
7.	HS300 relative strength index
8.	HS300 rising stock ratio
Factor 1,2,3 represent ordinary investors behavior.
Factor 4,5,6 represent leverage investor behavior.
Factor 7,8 represent market operation (represent market sentiment).
1 dependent variable (whether the stock price will rise or fall)
### Methodology
![alt text](https://github.com/DengQingqin/PHBS_TQFML-Sentiment-Measures-on-Stock-Market/blob/master/2.png "Logo Title Text 1")
For the result of logistic regression, when the number of sentiment factors equals to 2, we get the highest accuracy. After that, with the number of sentiment factors increasing, the predicting accuracy deceases. The most important 2 factors are A-share turnover rate and ETF net redemption rate. 
![alt text](https://github.com/DengQingqin/PHBS_TQFML-Sentiment-Measures-on-Stock-Market/blob/master/3.png "Logo Title Text 1")
The predicting result is very confusing.
![alt text](https://github.com/DengQingqin/PHBS_TQFML-Sentiment-Measures-on-Stock-Market/blob/master/4.png "Logo Title Text 1")
As for the result of SVM, when the number of sentiment factors equals to 6, we get the highest accuracy. Neither the training nor test accuracies are not very high, 0.730 for the training set and 0.545 for the test set. 
![alt text](https://github.com/DengQingqin/PHBS_TQFML-Sentiment-Measures-on-Stock-Market/blob/master/5.png "Logo Title Text 1")
Considering the sample size, K-fold cross-validation is used to check the generalization performance of the model. As we see, for the SVM, the accuracy score is volatile to some extent, varying from 0.467 to 0.607. The average accuracy score is 0.520, a little better than tossing a coin.
A_share turnover rate and ETF net redemption rate are proved to the top 2 important sentiment factors that may influence the stock market.
It is hard to predict the stock Index only depend on these sentiment factors.

