# Adaboost_Visualization
Visualize Adaboost parameter update process

1)&emsp;For every sample（$x_{1},x_{2},….,x_{N}$）, initialize all the weights uniformly, $w_{i}$=1/N for all i;

For t = 1, . . . , T:

{
    
2)&emsp;Fit the weak classiﬁer $G_t$ to the current weighted training set;
    
3)&emsp;Compute Weighted Error Rate for $G_t$ using $e_t=\sum_{i=1}^Nw_{i,t}I(y_i\not= G_t(x_i))$;

4)&emsp;Compute $G_t$'s weight $\alpha_t=0.5\log[(1-e_t)/e_t]$

5)&emsp;Update the weights as follows:$w_{i,t+1} = w_{i,t}exp({-α{G_{t}(x_{i})y(i) }})/Z_t$, where $Z_t=\sum_{i=1}^Nw_{i,t}$ 


}

6)&emsp;Compute the final predictions as: $f(x)=sign(\sum_{t=1}^T\alpha_tG_t(x_i))$
