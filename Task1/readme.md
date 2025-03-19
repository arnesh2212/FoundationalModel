
# Task 1 -  Multi-Class Classification

This Repository contains trained model to detect strong lensing images with no substructure, subhalo substructure, and vortex substructure using computer vision models. The models were trained using Pytorch and I also experimented with pre trained imagnet weighs for faster training.

## Results
 
| Model   |     Val AUC      
|----------|:-------------:|
| Resnet18 (Modified) |   0.9735   | 
| MaxVIT |  0.9789 | 


## The best AUROC Score is 0.9977 using MaxVIT
### Class 0 AUC: 0.997666
### Class 1 AUC: 0.996249
### Class 2 AUC: 0.999305
### Mean AUC: 0.9977

For multiclass the metric is calculated by iteratively treating each class as the positive class and all other classes as the negative, which is referred to as the one-vs-rest approach. One-vs-one is currently not supported by this metric. By default the reported metric is then the average over all classes, but this behavior can be changed by setting the average argument.

![alt text](https://github.com/arnesh2212/DeepLense/blob/main/Task1/ROC.png)

## Trained using multiple data augmentation techniques


## Other methods
- Reduction of learning rate on Plateau
- Cosine Annealing LR Scheduler


