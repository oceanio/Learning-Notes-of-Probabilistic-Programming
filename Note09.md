Notes on Chapter 5  
========================================

## Loss Functions

### squared-error loss  

![](images/Tex2Img_1375003014.png)  

### asymmetric squared-error loss function  

![](images/Tex2Img_1375098097.png)  

This represents that estimating a value larger than the true estimate is preferable to estimating a value below.  


### absolute-loss  

![](images/Tex2Img_1375098253.png)  

### zero-one loss  

![](images/Tex2Img_1375098487.jpg)  

### log-loss  

![](images/Tex2Img_1375098576.png)  

### other loss functions:  

![](images/Tex2Img_1375098686.png)  

This function emphasizes an estimate closer to 0 or 1 since if the true value θ is near 0 or 1, the loss will be very large unless θ^ is similarly close to 0 or 1.  

![](images/Tex2Img_1375098808.png)  

This function is bounded between 0 and 1 and reflects that the user is indifferent to sufficiently-far-away estimates. It is similar to the zero-one loss above, but not quite as penalizing to estimates that are close to the true parameter.  

## The risk of estimate θ^

![](images/Tex2Img_1375099707.png)  

+ If using the mean-squared loss, the Bayes action is the mean the posterior distribution
+ Whereas the median of the posterior distribution minimizes the expected absolute-loss.
+ In fact, it is possible to show that the MAP estimate is the solution to using a loss function that shrinks to the zero-one loss.  

For a specific trading signal, call it $x$, the distribution of possible returns has the form:

$$R_i(x) =  \alpha_i + \beta_ix + \epsilon $$

where $\epsilon \sim \text{Normal}(0, 1/\tau_i) $ and $i$ indexes our posterior samples. We wish to find the solution to 

$$ \arg \min_{r} \;\;E_{R(x)}\left[ \; L(R(x), r) \; \right] $$

according to the loss given above. This $r$ is our Bayes action for trading signal $x$. Below we plot the Bayes action over different trading signals.
