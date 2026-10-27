# CNN Flower Classification 🌸

## Project Overview

This project uses a Convolutional Neural Network (CNN) to classify flower images into five categories: Daisy, Dandelion, Roses, Sunflowers, and Tulips.

The model is built using TensorFlow and Keras. It learns visual features from flower images and predicts the flower category for a given input image.

## Objectives

- Build a CNN model for image classification.
- Preprocess and load flower images for training.
- Train and evaluate the model using training and validation datasets.
- Visualize model accuracy and loss.
- Predict the category of a sample flower image.
- Save the trained model for future use.

## Dataset

The project uses the **Flower Photos dataset**, containing five flower categories.

| Flower Category | Description |
|---|---|
| Daisy | Daisy flower images |
| Dandelion | Dandelion flower images |
| Roses | Rose flower images |
| Sunflowers | Sunflower images |
| Tulips | Tulip flower images |

**Dataset statistics:**

- Total images: 3,670
- Training images: 2,936
- Validation images: 734
- Image size: 180 × 180 pixels
- Batch size: 32
- Number of classes: 5

The dataset is organized into folders according to flower category.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- scikit-learn
- Jupyter Notebook

## Model Architecture

The CNN model consists of the following layers:

1. **Convolutional Layer:** Extracts visual features from flower images.
2. **Max Pooling Layer:** Reduces the spatial dimensions of feature maps.
3. **Convolutional and Max Pooling Layers:** Learn increasingly complex image features.
4. **Flatten Layer:** Converts feature maps into a one-dimensional vector.
5. **Dense Layer:** Learns patterns useful for classification.
6. **Dropout Layer:** Helps reduce overfitting during training.
7. **Output Layer:** Uses Softmax activation to predict probabilities for the five flower categories.

### Model Configuration

- Optimizer: Adam
- Loss function: Sparse Categorical Crossentropy
- Evaluation metric: Accuracy
- Epochs: 10
- Input image size: 180 × 180 pixels
- Output classes: 5

## Model Training and Evaluation

The model was trained using the training dataset and evaluated on the validation dataset.

### Results

| Metric | Result |
|---|---:|
| Training Accuracy | Approximately 92.03% |
| Validation Accuracy | Approximately 69.21% |
| Validation Loss | Approximately 1.2601 |
| Best Validation Accuracy | Approximately 70.16% |

The model achieved good accuracy on the training data. However, the difference between training and validation accuracy suggests overfitting. Further improvements could include data augmentation, additional regularization, and hyperparameter tuning.

## Output Visualizations

The project includes visualizations generated during model training and evaluation.

- `output_images/accuracy_plot.png` — Training and validation accuracy.
- `output_images/loss_plot.png` — Training and validation loss.
- `output_images/sample_prediction.png` — Example flower prediction.

## Sample Prediction

The trained model was tested using a sample flower image.

**Example result:**
- Predicted class: Daisy
- Prediction confidence: Approximately 84.31%

The prediction demonstrates how the trained CNN model classifies an input flower image.

## Project Structure

```text
CNN_Flower_Classification/
│
├── cnn_model.ipynb
├── README.md
├── requirements.txt
├── trained_model.h5
│
├── dataset/
│   └── flower_photos/
│       ├── daisy/
│       ├── dandelion/
│       ├── roses/
│       ├── sunflowers/
│       ├── tulips/
│       └── LICENSE.txt
│
└── output_images/
    ├── accuracy_plot.png
    ├── loss_plot.png
    └── sample_prediction.png
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/angelinvinnarasi-rgb/CNN_Flower_Classification.git
```

### 2. Navigate to the Project Folder

```bash
cd CNN_Flower_Classification
```

### 3. Create a Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open `cnn_model.ipynb` and run the cells in order.

**Note:** If the dataset is not available locally, follow the dataset-loading code in the notebook to download or locate it before training.

## Saved Model

The trained model is saved as:

`trained_model.h5`

It can be loaded using TensorFlow/Keras for further evaluation or prediction. Ensure that a compatible TensorFlow/Keras environment is installed.

## Future Improvements

- Apply data augmentation to improve generalization.
- Tune hyperparameters to improve validation accuracy.
- Experiment with deeper CNN architectures.
- Use transfer learning with pretrained models such as MobileNetV2.
- Test the model on additional flower images.
- Develop a simple web application for flower classification.

## Conclusion

This project demonstrates the application of Convolutional Neural Networks to image classification. The model successfully learns to classify flower images into five categories. The evaluation results also highlight the importance of reducing overfitting and improving generalization on unseen data.

## Author

**Elaiyarasi**

GitHub Repository: [CNN Flower Classification](https://github.com/angelinvinnarasi-rgb/CNN_Flower_Classification)
