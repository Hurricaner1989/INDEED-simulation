# INDEED Simulation
## About The Project
The main purpose of this project is to provide an intuition of the performance of INDEED method. Comparing the statistical outcomes of INDEED along with other methods/models, we can determine that when $n \geq p$, INDEED shows significantly better performance in predicting the true networks. However, when $n < p$, JDNIAC will have a better performance.

## Simulations
In this project, we mainly focus on $4$ simulations, which are when $n=25, p=100$, $n=50, p=100$, $n=100, p=10$ and $n=100, p=100$. In each simulation, we preform 5 loops and generate the box-plots based on the statistical outcomes.

## Results
### AUC
|![](n\=25\,p\=100/auc.png)|![](n\=50\,p\=100/auc.png)|
| -------------- | -------------- |
|![](n\=100\,p\=10/auc.png)|![](n\=100\,p\=100/auc.png)|

From the plots above, we can conclude that when $n \geq p$, INDEED with/without FDR have 

### Precision
|![](n\=25\,p\=100/precision.png)|![](n\=50\,p\=100/precision.png)|
| -------------- | -------------- |
|![](n\=100\,p\=10/precision.png)|![](n\=100\,p\=100/precision.png)|

### Recall
|![](n\=25\,p\=100/recall.png)|![](n\=50\,p\=100/recall.png)|
| -------------- | -------------- |
|![](n\=100\,p\=10/recall.png)|![](n\=100\,p\=100/recall.png)|

### Run Time
|![](n\=25\,p\=100/runtime.png)|![](n\=50\,p\=100/runtime.png)|
| -------------- | -------------- |
|![](n\=100\,p\=10/runtime.png)|![](n\=100\,p\=100/runtime.png)|