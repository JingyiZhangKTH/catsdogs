# Cats vs Dogs Classification Practice

This repository is a hands-on machine learning practice project.

I created it to strengthen my machine learning fundamentals by applying different classification methods to a simple Cats vs Dogs image dataset and comparing how they work.

## Goal

The goal of this project is not only to classify cats and dogs, but also to understand the differences between traditional machine learning methods and more modern vision models.

I started with basic approaches and gradually experimented with more advanced methods.

## What I practiced

### Traditional machine learning

I converted each image into a numerical feature vector by resizing the image and flattening its pixel values.

Then I experimented with several classical machine learning models:

- Linear Regression
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Support Vector Machine (SVM)

For each model, I trained it on the same Cats vs Dogs dataset and compared its predictions.

## Image Preprocessing

Before training the traditional machine learning models, the images were resized and converted into tensors.

For example, a `64 × 64` RGB image contains:

`3 × 64 × 64 = 12,288` pixel features.

The image is then flattened into a one-dimensional feature vector:

image -> flattened feature vector

I initially used `256 × 256` images, which resulted in:

`3 × 256 × 256 = 196,608` features per image.

This caused high memory usage, especially for KNN, because KNN calculates distances between samples.

Reducing the image size made the experiments much more manageable.


## Model Comparison

I trained different machine learning models on the same training dataset and compared their predictions on the same test images.

The test set is currently very small, with only 2 images for each cat and dog category, so I focused on inspecting individual predictions rather than relying only on accuracy.

## Prediction Visualization

I visualized every test image together with:

- the true label
- Logistic Regression prediction
- KNN prediction
- Decision Tree prediction
- SVM prediction

Example:

True: cat

Logistic Regression: cat
KNN: dog
Decision Tree: cat
SVM: cat

This made it easier to directly compare how different models behave on the same image.


```markdown
## PCA

I also explored Principal Component Analysis (PCA) as a way to reduce the dimensionality of the image data.

Instead of using thousands of raw pixel features, PCA can compress the feature space:

```text
12,288 dimensions
        ↓
       PCA
        ↓
  50–100 dimensions

This can reduce memory usage and make algorithms such as KNN and SVM more efficient.


```markdown
## Vision-Language Model

In addition to traditional machine learning, I experimented with a lightweight pretrained Vision-Language Model using Hugging Face Transformers.

The model receives both an image and a text prompt.

For example:

```text
Is this a cat or a dog?
Answer only: cat or dog.

Unlike the traditional machine learning models, the pretrained VLM does not need to be trained from scratch on my Cats vs Dogs dataset.
This allows me to compare:

Traditional ML
    ↓
trained on my own dataset

vs.

Pretrained Vision-Language Model
    ↓
zero-shot image understanding


```markdown
## Technologies Used

- Python
- PyTorch
- torchvision
- scikit-learn
- NumPy
- Matplotlib
- Hugging Face Transformers
- PIL

## What I Learned

Through this project, I practiced and learned about:

- image preprocessing
- feature vectors
- dimensionality
- train/test datasets
- linear regression
- logistic regression
- KNN
- decision trees
- SVM
- classification
- memory usage in high-dimensional data
- PCA
- prediction visualization
- model comparison
- Vision-Language Models
- zero-shot classification

## Current Limitations

The dataset used in this project is still small, especially the test set.

Because of this, the accuracy results should not be treated as reliable measurements of real-world performance.

At this stage, the main purpose of the project is learning and understanding how different machine learning methods work.


## Next Steps

I plan to continue this project by experimenting with:

- larger train / validation / test sets
- feature scaling
- confusion matrices
- precision, recall, and F1-score
- PCA
- Random Forest
- neural networks
- Convolutional Neural Networks (CNNs)
- data augmentation
- transfer learning
- pretrained vision models

The long-term goal is to compare the progression from traditional machine learning to deep learning and modern vision-language models.

