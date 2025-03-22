# This repositry contains the notebooks for task 6 - Foundation Model For Gravitational Lensing

### First a MAE (Masked Auto Encoder is pre-trained on the no_sub subset of the dataset, the MAE is a custom implementation which is based on the VIT architecture.
#### (Task6 - Foundational Model/mae_train.ipynb)

### Best Test loss - 5.296447373566931e-06 (MSE Error)

## Epoch 1 Results - 
![alt text](https://github.com/arnesh2212/GSOC---ML4SCI-Tasks/blob/main/Task6%20-%20Foundational%20Model/epoch1.png)
#### 16 Image Sampled, 1st column is the masked image, middle row is the decoded image and the 3rd column is the actual image.


## Epoch 100 Results - 
![alt text](https://github.com/arnesh2212/GSOC---ML4SCI-Tasks/blob/main/Task6%20-%20Foundational%20Model/best.png)
#### 16 Image Sampled, 1st column is the masked image, middle row is the decoded image and the 3rd column is the actual image.



# Resuls of MultiClass Classfication using the MAE PreTrained Encoder from above
### After 20 Epochs
### Accuracy - 99.44%
### AUC Macro : 0.9958 AUC Micro : 0.9958
![alt text](https://github.com/arnesh2212/GSOC---ML4SCI-Tasks/blob/main/Task6%20-%20Foundational%20Model/ROC_curve.png)

# Resuls of Super Resolution using MAE PreTrained Encoder from above and the Conv2DTranspose + Upsampling Blocks to convert the latent vector to the highr res image.
### MSE: 0.000090 - PSNR: 40.025167 - SSIM: 0.966675
### Models - https://drive.google.com/drive/folders/1J8nO6pwrbowHBE_RxFcK_r4Z9L8Lmid6?usp=sharing

