# Christmas project
2019-12-23

Actually, the model can be divided into three different parts:

(1) The prediction of `bid` and `ask`. Here we consider three different methods to construct model: OLS, Stepwise (backward) Selection, and Elastic Net. We construct model upon training dataset, and then we use the testing dataset to validate the performance. Here we use the `.score()` in Python to check the performance; the performance is better when the value of `score` is higher (note that `score` is between 0 and 1). After comparison, for `bid` of Stock A we use the Backward Selection, and for other `bid` of Stock B and `ask` we use the Elastic Net model.

(2) For `bidsz` and `asksz` , because the values are count variables, so here we consider Count (Poisson) Regression to fit the model. The results for the parameters are displayed in the result.

(3) For time intervals, here we first calculate the log values of then, and then use the Gaussian Mixture Model to fit the log-intervals (Using the hist plot, the distributions are close to Gaussian Mixture Distributions). Here we can find that the distribution of log time intervals are similar between Stock A and Stock B.

The generating process is sticked in the final part of the code file. 
