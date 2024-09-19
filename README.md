# Fine_Tuning_Image_Classification

### Task Description and Motivation

There would be two main steps during the homework:

Train from scratch a Convolutional Neural Network (CNN), such that is suited for binary classification on the cats_vs_dogs dataset (dataset details below). The original images have all different shapes, so have been resaphed to be 64x64.
Perform Parameter Efficient Fine-Tuning (PEFT) on this trained CNN, by using Low-Rank Adaptation (LoRA) on the leopards_vs_wolfs dataset (details below). The images are 32x32 and resaphed to be 64x64.
The main assumption of this fine-tuning task is based on the fact that both cats and leopards, as well as dogs and wolfs, belong to the same animal families of species (Felidae and Canidae respectively). Therefore I assumed that due to their shared biological traits, a model that was trained using cats and dogs data; could be also used to achieve good performance on distinguising between leopards and wolfs, by performing PEFT to the original model through LoRA.

### Dataset Description

For this homework, I will be using two well-known image classification datasets:

TensorFlow Dataset cats_vs_dogs. Data Size: about 12K images per animal (around 24K images in total), from which 80% are used for training, 10% for validating during training and 10% for final testing.
Subset of TensorFlow Dataset CIFAR100 considering only classes 42 (leopard) and 97 (wolf). From here onwords I will refer to this dataset as leopards_vs_wolfs. Data Size: 600 images for each animal (1200 images in total) from which 80% are used for training, 10% for validating during training and 10% for final testing. The images are 32x32 and have been augmented to be 64x64.
