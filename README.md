# INDEED Simulation
## About The Project
The main purpose of this project is to provide an intuition of the performance of [INDEED](https://github.com/ressomlab/INDEED) version 2.3.1, compared to other competing methods. We select [DNAPATH](https://cran.r-project.org/web/packages/dnapath/index.html) version 0.7.4 and [JDINAC](https://github.com/jijiadong/JDINAC) for comparison since they are both based on the idea of partial correlation, similiar to INDEED. For INDEED, we include the results with and without FDR correction. In practice, it's an option for users to decide. The simulatioin covers a wide range of $n, p$ combinations, it's supposed to tell us the performance of each method under $n < p$, $n = p$, and $n > p$ scenarios. We compute precision recall AUC, precision, recall and run time as the metrics. From our simulation, INDEED has the best performance when $n > p$, and $n = p$, while JDINAC works the best when $n < p$.

## More Details About The Simulations
In the simulation, we mainly focus on $4$ pairs of $n, p$ combination, which are $n = 25, p = 100$, $n = 50, p = 100$, $n = 100, p = 100$, and $n = 100, p = 10$. We limit the $p$ value up to $100$ since a higher value usually result in a much longer time to run for INDEED. Ideally, we would like to optimize INDEED to run a few minutes for $p$ around $1000$, this is one future work on our task list. Right now, users should comfortably run INDEED with $p$ around $100$ in only a few minutes or less. We also test $n = 10, p = 100$ in the simulation. However, this combination seems to exceed the limit of most methods in our comparisons. We decide to exclude it in the following boxplots. For each $n, p$ combination, we run $10$ loops and generate the box-plots based on the metrics of precision recall AUC, precision, recall and run time. We recommend users who are interetsed in more loops to take our simulation codes and try it by themselves. 

## Results
### Precision Recall AUC
|![](Simulation/n\=25\,p\=100/auc.png)|![](Simulation/n\=50\,p\=100/auc.png)|
| -------------- | -------------- |
|![](Simulation/n\=100\,p\=100/auc.png)|![](Simulation/n\=100\,p\=10/auc.png)|

JDINAC returns a ranking list of edges. Precision recall AUC is the better metric to compare different methods with a ranking output.

### Precision
|![](Simulation/n\=25\,p\=100/precision.png)|![](Simulation/n\=50\,p\=100/precision.png)|
| -------------- | -------------- |
|![](Simulation/n\=100\,p\=100/precision.png)|![](Simulation/n\=100\,p\=10/precision.png)|

JDINAC returns a ranking list of edges with numb value as the score. We take all edges with numb > 0 as a positive prediction. This might be unfair to JDINAC. Precision recall AUC is probably the better metric to compare.

### Recall
|![](Simulation/n\=25\,p\=100/recall.png)|![](Simulation/n\=50\,p\=100/recall.png)|
| -------------- | -------------- |
|![](Simulation/n\=100\,p\=100/recall.png)|![](Simulation/n\=100\,p\=10/recall.png)|

Similar to Precision, JDINAC returns a ranking list of edges with numb value as the score. We take all edges with numb > 0 as a positive prediction. This might be unfair to JDINAC. Precision recall AUC is probably the better metric to compare.

### Run Time
|![](Simulation/n\=25\,p\=100/runtime.png)|![](Simulation/n\=50\,p\=100/runtime.png)|
| -------------- | -------------- |
|![](Simulation/n\=100\,p\=100/runtime.png)|![](Simulation/n\=100\,p\=10/runtime.png)|
