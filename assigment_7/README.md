# Assignment 7 – Comparison of VGG16 and EfficientNetB0 Using Transfer Learning

## Objective

The objective of this assignment is to implement and compare two pretrained Convolutional Neural Network (CNN) architectures, **VGG16** and **EfficientNetB0**, for image classification using the **CIFAR-10 dataset**.

The assignment demonstrates the use of **Transfer Learning**, where pretrained ImageNet models are used as feature extractors and new classification layers are added for the CIFAR-10 classification task.

## Dataset

The **CIFAR-10 dataset** is used for this assignment.

CIFAR-10 contains color images belonging to **10 different classes**.

The dataset consists of:

* 50,000 training images
* 10,000 testing images
* 10 image classes
* Original image size: 32 × 32 pixels
* RGB color images

The images are resized to **224 × 224 pixels** so that they can be processed by the pretrained VGG16 and EfficientNetB0 models.

## Steps Performed

1. Checked GPU availability using TensorFlow.
2. Imported the required Python and TensorFlow libraries.
3. Loaded the CIFAR-10 dataset.
4. Converted the class labels into one-hot encoded format.
5. Created TensorFlow data pipelines for training and testing.
6. Shuffled the training dataset.
7. Resized images from 32 × 32 to 224 × 224 pixels.
8. Batched and prefetched the datasets for efficient processing.
9. Loaded VGG16 with pretrained ImageNet weights.
10. Froze the VGG16 base layers.
11. Added a new classification head for the 10 CIFAR-10 classes.
12. Trained the VGG16-based model for 3 epochs.
13. Loaded EfficientNetB0 with pretrained ImageNet weights.
14. Froze the EfficientNetB0 base layers.
15. Added a new classification head for CIFAR-10.
16. Trained the EfficientNetB0-based model for 3 epochs.
17. Evaluated both models on the test dataset.
18. Compared the accuracy of VGG16 and EfficientNetB0.

## Transfer Learning

Transfer learning allows a model that has already learned useful image features from a large dataset to be reused for another image classification task.

In this assignment:

* VGG16 is loaded with ImageNet pretrained weights.
* EfficientNetB0 is loaded with ImageNet pretrained weights.
* The original classification layers are removed.
* The pretrained convolutional layers are frozen.
* New fully connected layers are added for CIFAR-10 classification.

This approach allows the pretrained models to act as feature extractors while the newly added layers learn to classify the CIFAR-10 classes.

## VGG16 Model

The VGG16 model uses:

* Pretrained ImageNet weights
* Frozen convolutional base
* Global Average Pooling
* Dense layer with 256 neurons
* ReLU activation
* Dropout of 0.5
* Output layer with 10 neurons
* Softmax activation

## EfficientNetB0 Model

The EfficientNetB0 model uses:

* Pretrained ImageNet weights
* Frozen convolutional base
* Global Average Pooling
* Dense layer with 256 neurons
* ReLU activation
* Dropout of 0.5
* Output layer with 10 neurons
* Softmax activation

## Model Configuration

Both models use:

* **Input Image Size:** 224 × 224 × 3
* **Batch Size:** 32
* **Optimizer:** Adam
* **Loss Function:** Categorical Crossentropy
* **Number of Classes:** 10
* **Training Epochs:** 3
* **Dropout:** 0.5

## Model Evaluation

Both models are evaluated using classification accuracy on the CIFAR-10 test dataset.

The final accuracy values are displayed and stored in a Pandas DataFrame so that the performance of VGG16 and EfficientNetB0 can be compared easily.

## Result

The notebook compares the following two models:

| Model          | Evaluation Metric |
| -------------- | ----------------- |
| VGG16          | Test Accuracy     |
| EfficientNetB0 | Test Accuracy     |

The exact accuracy values are obtained when the notebook is executed and are displayed in the final comparison table.

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* CIFAR-10
* VGG16
* EfficientNetB0
* Google Colab / Jupyter Notebook

## Project Structure

```text
Assignment-7/
│
├── ass_7_DL.ipynb
└── README.md
```

## How to Run

### Step 1: Open the Notebook

Open `ass_7_DL.ipynb` using **Google Colab** or Jupyter Notebook.

### Step 2: Enable GPU

If using Google Colab, a GPU can be enabled from:

```text
Runtime → Change runtime type → Hardware accelerator → GPU
```

### Step 3: Run the Notebook

Execute the cells in order to:

1. Check GPU availability.
2. Load the CIFAR-10 dataset.
3. Preprocess the images and labels.
4. Build the VGG16 model.
5. Train the VGG16 model.
6. Build the EfficientNetB0 model.
7. Train the EfficientNetB0 model.
8. Evaluate both models.
9. Compare their accuracy.

## Conclusion

This assignment demonstrates the practical use of **Transfer Learning for image classification**.

Two pretrained CNN architectures, **VGG16** and **EfficientNetB0**, are adapted for the CIFAR-10 classification problem. Their pretrained convolutional layers are frozen, while newly added classification layers are trained for the 10 CIFAR-10 classes.

Finally, the performance of both models is evaluated and compared using their test accuracy.
