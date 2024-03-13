
# Task 1 -  Multi-Class Classification

This Repository contains trained model to detect strong lensing images with no substructure, subhalo substructure, and vortex substructure using computer vision models. The models were trained using Pytorch and I also experimented with pre trained imagnet weighs for faster training.

## Results
 
| Model   |     Val AUC      |  Train AUC |
|----------|:-------------:|------:|
| MobileNetV2 |  0.9741 | 0.9999 |
| Resnet50 (Modified) |    0.9724   |  0.9894 |
| MobileNetV3Large | 0.9983 |  0.9916  |

![alt text]([https://github.com/arnesh2212/DeepLense/blob/main/Task1%20-%20Classification/1.png](https://github.com/arnesh2212/DeepLense/blob/main/Task1%20-%20Classification/Screenshot_20240313_095651.png))

## Some Data Augmentation Methods used -
-     transforms.RandomHorizontalFlip(),
-     transforms.RandomVerticalFlip(),
-     transforms.RandomRotation([-90,90]),


## Other methods
- Reduction of learning rate on Plateau
- Cosine Annealing LR Scheduler


### Trained Model weights are present in this Repository
