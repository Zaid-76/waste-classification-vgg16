# Waste Classification with VGG16

I worked on this project as part of an IBM / Skills Network course. The goal was
to classify images of **organic** and **recyclable** waste using a pretrained VGG16 model.

The notebook includes image augmentation, a classifier trained on frozen VGG16
features, and a second experiment with the last convolutional layer unfrozen.
It also compares predictions from the saved models using classification reports
and sample images.

## Run

Open [Waste_Classification_VGG16.ipynb](Waste_Classification_VGG16.ipynb) in Jupyter
or Google Colab and run the cells in order. The setup cell installs the libraries,
and the data cell downloads the reduced course dataset. Restart the kernel after
installation if needed. Training saves model checkpoints in the working directory.

The code follows the course experiment settings: five training batches per epoch,
a 20% validation split, and evaluation on 50 test images per class. The second model
is initialized separately rather than resumed from the first trained classifier.

## Dataset and credit

The course dataset is a reduced version of
[Waste Classification Data](https://www.kaggle.com/datasets/techsash/waste-classification-data).

Based on the IBM / Skills Network final project, *Classify Waste Products Using
Transfer Learning*. Original course material: Copyright © IBM Corporation.
All rights reserved.
