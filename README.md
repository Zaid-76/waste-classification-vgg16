# Waste Classification with VGG16

I completed this project as part of an IBM / Skills Network course. It uses a
pretrained VGG16 model to classify waste images as **organic (O)** or **recyclable (R)**.

The notebook covers data augmentation, training a classifier on frozen VGG16
features, experimenting with an unfrozen convolutional layer, and comparing
predictions on test images.

## Results

On the 100 test images used in the notebook (50 from each class):

| Experiment | Accuracy |
| --- | ---: |
| Feature extraction | 79% |
| Unfrozen-layer experiment | 78% |

The second experiment builds a separate model with `block5_conv3` unfrozen,
rather than continuing from the first trained classifier.

## Run the notebook

Open [Waste_Classification_VGG16.ipynb](Waste_Classification_VGG16.ipynb) in Jupyter
or Google Colab and run the cells in order. The notebook installs the main
libraries and downloads the reduced course dataset. If `requests` or `tqdm` is
missing, install it with `pip install requests tqdm`.

Training creates model checkpoints in the working directory. The original code
and saved outputs are kept in this version; the course submission prompts have
been removed and the headings tidied.

## Dataset and credit

- [Waste Classification Data](https://www.kaggle.com/datasets/techsash/waste-classification-data)
- Based on the IBM / Skills Network final project, *Classify Waste Products Using Transfer Learning*.

Original course material: Copyright © IBM Corporation. All rights reserved.
