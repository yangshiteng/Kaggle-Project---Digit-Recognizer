# Kaggle-Project---Digit-Recognizer

MNIST ("Modified National Institute of Standards and Technology") is the de facto “hello world” dataset of computer vision. Since its release in 1999, this classic dataset of handwritten images has served as the basis for benchmarking classification algorithms. As new machine learning techniques emerge, MNIST remains a reliable resource for researchers and learners alike.

# Goal

In this Kaggle project, the goal is to correctly identify digits from a dataset of tens of thousands of handwritten images. 

# Metric

This competition is evaluated on the categorization accuracy of your predictions (the percentage of images you get correct).

# Data Description

The data files train.csv and test.csv contain gray-scale images of hand-drawn digits, from zero through nine.

Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255, inclusive.

The training data set, (train.csv), has 785 columns. The first column, called "label", is the digit that was drawn by the user. The rest of the columns contain the pixel-values of the associated image.

Each pixel column in the training set has a name like pixelx, where x is an integer between 0 and 783, inclusive. To locate this pixel on the image, suppose that we have decomposed x as x = i * 28 + j, where i and j are integers between 0 and 27, inclusive. Then pixelx is located on row i and column j of a 28 x 28 matrix, (indexing by zero).

For example, pixel31 indicates the pixel that is in the fourth column from the left, and the second row from the top, as in the ascii-diagram below.

Visually, if we omit the "pixel" prefix, the pixels make up the image like this:

![345](https://user-images.githubusercontent.com/60442877/132073956-02debb31-593b-4e80-90af-2420140b08f3.jpg)

The test data set, (test.csv), is the same as the training set, except that it does not contain the "label" column.

# Data Preparation

1. check for null and missing values
2. Normalization (CNN converg faster on [0..1] data than on [0..255])
3. Reshape
4. Label Encoding
5. Split training and validation set

# Model Descprition 

This is a 5 layers Sequential Convolutional Neural Network for digits recognition trained on MNIST dataset. 
I choosed to build it with keras API (Tensorflow backend) which is very intuitive

1. RMSprop as the optimizer
2. Annealing method of the learning rate
3. Data Augmentation
    * Randomly rotate some training images by 10 degrees
    * Randomly Zoom by 10% some training images
    * Randomly shift images horizontally by 10% of the width
    * Randomly shift images vertically by 10% of the height







