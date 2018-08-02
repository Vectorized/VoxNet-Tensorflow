# VoxNet Tensorflow
A Tensorflow Implementation of VoxNet (dimatura.net/research/voxnet/).  

## Pre-trained Weights
Pre-trained weights are provided under the `checkpoints` directory.  
This network is pretty small, under 1 million parameters, which is less than 10MB in size.

## Dataset
A pre-voxelized ShapeNet40 (http://modelnet.cs.princeton.edu/) is already provided in `volumetric_data.zip`.  
It is directly converted from the matlab files included in (http://vision.princeton.edu/projects/2014/3DShapeNets/3DShapeNetsCode.zip)  
Each example is a .npy file. To visualize a voxel .npy file, go to (http://bkys.io/voxvis).

## Modifications
No dropout is used for faster training.  
Batch normalization is used after every layer, except the last fully connected layer.  
Network is all-convolutional.

## Requirements
Python (>= 2.7 or >= 3), Tensorflow (>= 1.0) and numpy (>= 1.0). 

## How To Use
Run `voxnet_train.py` to train the model.  
Run `voxnet_test.py` to test the average accuracy.

## Accuracy
After 20 minutes of training from scratch on a Nvidia Titan X, it is able to get 86%+ test accuracy.