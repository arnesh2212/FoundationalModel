
# Task 3A-  Image Super-resolution 


This Repository contains a trained model to upscale low-resolution strong lensing images using the provided high-resolution samples as ground truths. The models were trained using Pytorch for more flexibility.

## Results
 
| Model   |     Val MSE      |  Val PSNR | Val SSIM |
|----------|:-------------:|------:|------:|
| HAT |  5.9671598e-05     | 42 | 0.975 |
| DIPNet |  5.846322436030497e-05 | 42.4 | 0.977 |

## Model_training - https://github.com/arnesh2212/DeepLense/blob/main/Task3%20-%20SuperResolution/task3.ipynb
## Model_training of HAT- https://github.com/arnesh2212/DeepLense/blob/main/Task3%20-%20SuperResolution/task3.ipynb

![alt text](https://github.com/arnesh2212/DeepLense/blob/main/Task3%20-%20SuperResolution/2.png)

### Trained Model weights are present in this Repository
### Reference - https://github.com/xiumu00/DIPNet
### DIPNet Is a efficient algorithm which provides exceptional performance for Less Compute Power
### Other Models that were tried are - ESRGAN, SRGAN , SRCNN and SRResnet
