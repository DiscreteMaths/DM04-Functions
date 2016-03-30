Geographically Weighted Regression.
===================================


In this essay I will provide some information about Geographically Weighted Regression which is excellent tool for testing model specification.
To understand (GWR) and its methodology we should know regression and spatial analysis. At the beginning the aim of data analysis is to provide relationship between two variables.

### Regression.
Actually, ***regression*** is the most common type to obtain this aim. *If* we want to define regression, we will say is the statistical measure that attempts to determine relationship between one dependent variable and many others changing variables.
![Alt text](http://image.slidesharecdn.com/simplelinearregressionpelatihan-090829234643-phpapp02/95/simple-linier-regression-9-728.jpg?cb=1251589640)
### Spatial Analysis
In spatial analysis the data pulled from geographical units and a single regression equation is estimated we assume a stationary process. What is happening has an impact in producing average or global parameter estimates. 
Usually the least squares method is used to estimate B_ks as what we done here. As the maximum likelihood estimate of B .


B ̀=(x^t*x)^(-1)x^t*y  
This method is applied to geographical data is that each case corresponds to geographical location.

The assumption of stationarity in regression is:
y=∝+Bx.
Assumption is that the values are the same everywhere.
The measured relationships ***vary spatially*** because several points.
<ol>
<li>Sampling variation. </li>
<li>, Relationships intrinsically different across space.</li>
<li>Model misspecification.</li>
</ol>

**Note**: If there is spatial nonstationary, we only see it through the residuals not directly because (GWR).

###Geographically weighted regression.
Is an exploratory technique mainly intended to indicate where non-stationarity is taking place on the map, that is where locally weighted regression coefficients move away from their global values. ‘It’s basis is the concern that the fitted coefficient values of a global model, fitted to all the data may not represent detailed local variations in the data adequately’.
y=B+B*x+....+ε.   and  (B(u)) ̀=(x^t* W(u)x)^(-1) x^t*W(u)y.
Where W(u) is a square matrix of weights specific to location u in the study area, X^T* W(u)*X is the geographically weighted variance-covariance matrix, and y is the vector of the values of the dependent variable.
The weight matrix W(u) contains the geographically weights in its leading diagonal and 0 in its off diagonal elements which is helpful for investigating the precision of spatially varying estimates .
The weight matrix W(u) contains the geographically weights in its leading diagonal and 0 in its off diagonal elements which is helpful for investigating the precision of spatially varying estimates .

![Alt text](http://docsdrive.com/images/ansinet/jas/2011/img2-2k11-630-638.gif)

Where W is the weight given to data point n for the estimate of the local parameters at location u. In fact this matrix is the key output of GWR. By selecting individual rows, it is possible to see how a coefficient corresponding to a given predictor variable changes geographically. More than that, this is possible to find the stander error of coefficient estimate.
Numerous weighting schemes can be used although they tend to be Gaussian.

###Gaussian.

![Alt text](http://www.mdpi.com/remotesensing/remotesensing-07-06454/article_deploy/html/images/remotesensing-07-06454-g003.png)

![Alt text](http://i.imgur.com/mp1D5.jpg)






