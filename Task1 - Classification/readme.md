
# Task 1 -  Multi-Class Classification

This Repository contains trained model to detect strong lensing images with no substructure, subhalo substructure, and vortex substructure using computer vision models. The models were trained using Pytorch and I also experimented with pre trained imagnet weighs for faster training.

## Results
 
| Model   |     Val AUC      |  Train AUC |
|----------|:-------------:|------:|
| MobileNetV2 |  0.9741 | 0.9999 |
| Resnet50 (Modified) |    0.9724   |  0.9894 |
| MobileNetV3Large | 0.0.9883 |  0.9916  |

## The best AUROC Score is 0.9983 and the best AUC Score is 0.9883 with above 98% accuracy

For multiclass the metric is calculated by iteratively treating each class as the positive class and all other classes as the negative, which is referred to as the one-vs-rest approach. One-vs-one is currently not supported by this metric. By default the reported metric is then the average over all classes, but this behavior can be changed by setting the average argument.


![alt text](https://github.com/arnesh2212/DeepLense/blob/main/Task1%20-%20Classification/Screenshot_20240313_095651.png)

## Some Data Augmentation Methods used -
-     transforms.RandomHorizontalFlip(),
-     transforms.RandomVerticalFlip(),
-     transforms.RandomRotation([-90,90]),


## Other methods
- Reduction of learning rate on Plateau
- Cosine Annealing LR Scheduler


### Trained Model weights are present in this Repository
