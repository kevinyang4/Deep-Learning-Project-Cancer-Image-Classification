# COMP432-Project

Google Colab: https://colab.research.google.com/drive/1nqzqEwi1e2bP_yq9nRnrSJUz2QEXUaZc?usp=sharing 

## Team member contribution


## Description
The main objective of this project is to study the transferability of CNN models between different types of datasets. It is important to gain an understanding of transferability in machine learning as it allows for faster model training through and an efficient use of resources. This project includes two tasks to solve this problem: 

Task 1: Train a CNN model for Colorectal Cancer Classification, evaluating its performance through training accuracy and loss metrics. To understand the learned feature representations, t-SNE is applied to the CNN encoder's output features, visualizing them in reduced dimensions based on their class labels. This provides insights into the quality and class separability of the learned features.

Task 2: Compare the feature extraction capabilities between the CNN encoder trained in Task 1 and a pre-trained ImageNet encoder on two new datasets, Dataset 2 and Dataset 3. Features extracted from these encoders are visualized using t-SNE to analyze their generalization across domains. SVM is used to classify the extracted features, assessing their discriminative power for each dataset.

## How to run code
Open the .ipynb file and import all three datasets. The code can then be run on CPU/GPU. There are two seperate code blocks, one for each task. To run the project, first run the imports located in the first code block. After you can run the 'Task 1' code block which contains the data preprocessing and the setup for the ResNet18 model. The model is trained and evaluated in this task. The hyperparameter tuning is also ran in this code block. The results are also analyzed and visualized with Grad-Cam. The 'Task 2' code block contains the feature extraction from the encoders from 'Task 1' and plot t-SNE graphs. This code block will also classify the extracted features using Support Vector Machine and output its Classification reports.

## How to train/validate model
The ResNet18 model is trained and validated in 'Task 1' when the corresponding code block is ran. The SVM model is trained and validated in 'Task 2' when the corresponding code block is ran.


## How to run pre-trained model on the provided sample test dataset
The code to run the pre-trained model is located in the 'Task 2' code block. All you need to do is run the corresponding code block. Make sure that this code block successfully runs.
```
# Extract features for Dataset 2
features2_task1, labels2_task1 = extract_features(encoder_task1, dataloader2)

# Extract features for Dataset 3
features3_task1, labels3_task1 = extract_features(encoder_task1, dataloader3)
```

```
# Extract features for Dataset 2
features2_imagenet, labels2_imagenet = extract_features(imagenet_encoder, dataloader2)

# Extract features for Dataset 3
features3_imagenet, labels3_imagenet = extract_features(imagenet_encoder, dataloader3)
```

## Description on how to obtain the Dataset from an available download link
Head over to the link on the [dataset1](https://onedrive.live.com/?authkey=%21ADmb8ZdEzwFMZoo&id=FB338EA7CF297329%21405133&cid=FB338EA7CF297329&parId=root&parQt=sharedby&o=OneUp), [dataset2](https://onedrive.live.com/?authkey=%21APy4wecXgMnQ7Kw&id=FB338EA7CF297329%21405132&cid=FB338EA7CF297329&parId=root&parQt=sharedby&o=OneUp), and [dataset3](https://onedrive.live.com/?authkey=%21AKqEWb1GDjWPbG0&id=FB338EA7CF297329%21405131&cid=FB338EA7CF297329&parId=root&parQt=sharedby&o=OneUp) respectively and click on "Download".

The .zip files can then be imported to the Google Colab, unzipped, and used to run the code.
