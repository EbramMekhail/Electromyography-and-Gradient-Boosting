# Electromyography and Gradient Boosting



## What is Gradient Boosting?

<br>

The best way to describe *Gradient Boosting* would the combination of multiple smaller models into a single composite model. In *Gradient Boosting* the method they use to create a single model is by taking the previous model and fitting it to the residual error made by the previous model.

The following equations describes the process.
1. $F_1(X) = y$ - Fitting Data into a model.
2. $h_1(X) = y - F_1(X)$ - Fitting the previous model to the residual error.
3. $F_2(X) = F_1(X) + h_1(X)$ - Creating a new model based on the previous model and the residual error
4. $F_{m+1}(X) = F_m(X) + h_m(X)$ - Repeats steps 2-3. The models residual error for m iterations: <br> $h_m(X) = y - F_m(X)$
   
---
## Heading in the right direction

In the previous section we explained how Gradient Boosting works weak models trained on previous models residual error $y-F_{m-1}(x)$. The issue arises when the model chases outliers. 