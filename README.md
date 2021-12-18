# Masked Facial Reconstruction using GAN models
This repository is mainly built on Pytorch.
Dataset can be downloaded from https://www.kaggle.com/prasoonkottarathil/face-mask-lite-dataset

## This repository contains 3 python notebook files.
1. VAE
2. VAE + DCGAN
3. VAE + PIX2PIX

## Each of these python notebook files does 3 things.
1. Train a model for 10 epochs and generate an image every 20 batches.
2. Calculate MSE and L1 loss using validation set.
3. Generate 2 images from 2 masked images in validation set.

### These notebooks were made on Kaggle. Therefore, every path are define to be compatible with Kaggle server.
Every input to be read starts with '../input/'
Every output starts with './'

## Pretrained models
Pretrained models are in folder 'saved_models'
### For VAE model, it is named 'unet.pth'
### For VAE + DCGAN, there are two pretrained models
1. 'dcgan_generator_lambda1.pth' for vae+dcgan with lambda_pixel=1
2. 'dcgan_generator_lambda100.pth' for vae+dcgan with lambda_pixel=100
### For VAE + PIX2PIX, there are two pretrained models
1. 'pix2pix_generator_lambda1.pth' for vae+dcgan with lambda_pixel=1
2. 'pix2pix_generator_lambda100.pth' for vae+dcgan with lambda_pixel=100

## Inferencing
Each notebook has an inference block after loading model at nearly the end of the notebook.
In order to execute the block, you need to 
1. Change file path.
2. Execute the first 8 blocks in order to import libraries, create inference model object and create dataloaders.
