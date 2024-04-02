
# GSOC 2024 - DeepLense

This Repository contains the solutions for the tasks for the project - Superresolution for Strong Gravitational Lensing

## This repository contains 3 folders which have solutions for Task 1,3A and 3B

The files are in the form of jupyter Notebooks which and i ahve also included weights of all the required models.
## 🚀 About Me
Hi, I am a Computer Science student at IIITD, and I love to work with projects that are ambitious and intgrated lastest technology like machine learning and deep learning to solve classcial problems.

# Task 1 -  Multi-Class Classification

This Repository contains trained model to detect strong lensing images with no substructure, subhalo substructure, and vortex substructure using computer vision models. The models were trained using Pytorch and I also experimented with pre trained imagnet weighs for faster training.

## Results
 
| Model   |     Val AUC      |  Train AUC |
|----------|:-------------:|------:|
| MobileNetV2 |  0.9741 | 0.9999 |
| Resnet50 (Modified) |    0.9724   |  0.9894 |
| MobileNetV3Large | 0.998 |  0.9916  |

## The best AUROC Score is 0.9978 with 98.3% accuracy
### Class 0 AUC: 0.997853
### Class 1 AUC: 0.996304
### Class 2 AUC: 0.999095
### Mean AUC: 0.999

For multiclass the metric is calculated by iteratively treating each class as the positive class and all other classes as the negative, which is referred to as the one-vs-rest approach. One-vs-one is currently not supported by this metric. By default the reported metric is then the average over all classes, but this behavior can be changed by setting the average argument.

## Task1 - https://github.com/arnesh2212/DeepLense/blob/main/Task1%20-%20Classification/task1.ipynb
![alt text](https://github.com/arnesh2212/DeepLense/blob/main/Task1%20-%20Classification/roc.png)

## Some Data Augmentation Methods used -
-     transforms.RandomHorizontalFlip(),
-     transforms.RandomVerticalFlip(),
-     transforms.RandomRotation([-90,90]),


## Other methods
- Reduction of learning rate on Plateau
- Cosine Annealing LR Scheduler


### Trained Model weights are present in this Repository




# Task 3A-  Image Super-resolution 


This Repository contains a trained model to upscale low-resolution strong lensing images using the provided high-resolution samples as ground truths. The models were trained using Pytorch for more flexibility.

## Results
 
| Model   |     Val MSE      |  Val PSNR | Val SSIM |
|----------|:-------------:|------:|------:|
| HAT |  5.9671598e-05     | 42 | 0.975 |
| DIPNet |  5.846322436030497e-05 | 42.4 | 0.977 |

![alt text](https://github.com/arnesh2212/DeepLense/blob/main/Task3%20-%20SuperResolution/2.png)

### Trained Model weights are present in this Repository
### Reference - https://github.com/xiumu00/DIPNet
### DIPNet Is a efficient algorithm which provides exceptional performance for Less Compute Power
### Other Models that were tried are - ESRGAN, SRGAN , SRCNN and SRResnet


# Task 3B-  Image Super-resolution 


This Repository contains the trained model to upscale low-resolution strong lensing images using the provided high-resolution samples as ground truths. The models were trained using Pytorch for more flexibility.
The techniques ranged from using simple CNN-based scaling techniques to using zero-shot learning techniques.
The future scope of this project is to use latent variable-based models and GAN-based architectures.

## Results
 
| Model   |     Val MSE      |  Val PSNR | Val SSIM |
|----------|:-------------:|------:|------:|
| DIPNet |  0.0009894068 | 31.1011 | 0.6178 |
| ZSSRNet | 0.0018982704 | 33.650 | 0.8366753 |
| WaveMixSR |  0.00044689313 | 34.2668 |  0.85012 |
| SRGAN (Gen Only) |   0.0003597185 | 36.95 |  0.902 |


Training on the full dataset gives a substantial jump in the performance due to the less amount of data
| Model   |     Val MSE      |  Val PSNR | Val SSIM |
|----------|:-------------:|------:|------:|
| SRGAN (Gen Only) |   4.818466e-05 |44.1 |  0.974 |


## The following are some example images in the dataset - 

![alt text](https://github.com/arnesh2212/DeepLense/blob/main/Task3B%20-%20RealiImages%20SuperResolution/eg1.png)
![alt text](https://github.com/arnesh2212/DeepLense/blob/main/Task3B%20-%20RealiImages%20SuperResolution/eg2.png)

## Some Techniques like gaussian blur and fastn1Denoising can also be used to improve further performance



### Trained Model weights are present in this Repository
reference - https://github.com/leftthomas/SRGAN/tree/master


## License

[MIT](https://choosealicense.com/licenses/mit/)

## References - 
https://paperswithcode.com/method/mobilenetv2
https://arxiv.org/abs/1512.03385
https://paperswithcode.com/method/mobilenetv3
https://paperswithcode.com/task/image-super-resolution
https://towardsdatascience.com/super-resolution-a-basic-study-e01af1449e13
https://github.com/lusinlu/gradient-variance-loss
https://www.sciencedirect.com/science/article/abs/pii/S0030402623002462#:~:text=Therefore%2C%20the%20pixel%20loss%20gradually,resolution%20to%20get%20higher%20PSNR.
https://arxiv.org/abs/2205.04437
https://github.com/leftthomas/SRGAN/tree/master
