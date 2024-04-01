
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
