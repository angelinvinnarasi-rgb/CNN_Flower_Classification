# CNN Flower Image Classification

## Project Overview
This project uses a Convolutional Neural Network (CNN) to classify flower images into five categories using TensorFlow and Keras.

## Objectives
- Build and train a CNN model for image classification.
- Classify images into five flower categories.
- Evaluate the model using accuracy, loss, and classification metrics.
- Visualize training performance and sample predictions.

## Dataset
The dataset contains 3,670 flower images across five categories:
- Daisy
- Dandelion
- Roses
- Sunflowers
- Tulips

Dataset source:
https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz

The dataset was divided into:
- Training images: 2,936
- Validation images: 734

## Technologies Used
- Python
- TensorFlow and Keras
- NumPy
- Matplotlib
- Scikit-learn
- Pillow
- Jupyter Notebook

## Model Architecture
The CNN model includes:
1. Three convolutional layers with ReLU activation.
2. Max-pooling layers.
3. A flatten layer.
4. A dense layer with 128 neurons.
5. A dropout layer to help reduce overfitting.
6. An output layer with five neurons and softmax activation.

Image size: 180 x 180 pixels  
Batch size: 32  
Epochs: 10  
Optimizer: Adam  
Loss function: Sparse categorical cross-entropy

## Model Performance
- Final training accuracy: approximately 92.03%
- Final validation accuracy: approximately 69.21%
- Best validation accuracy: approximately 70.16%

The difference between training and validation accuracy suggests overfitting. Further improvements could include data augmentation, transfer learning, and additional tuning.

## Evaluation
The model was evaluated using a classification report with precision, recall, and F1-score for each flower category.

## Output Images
The `output_images` folder contains:
- `accuracy_plot.png` — training and validation accuracy.
- `loss_plot.png` — training and validation loss.
- `sample_prediction.png` — example flower prediction.

A sample image was correctly predicted as Daisy with approximately 84.31% confidence.

## How to Run
1. Install Python and Jupyter Notebook.
2. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

3. Open `cnn_model.ipynb` in Jupyter Notebook.
4. Run the notebook cells in order to prepare the dataset, train the model, and evaluate predictions.

Ensure the dataset path in the notebook points to the dataset folder included with this project, or update it to the downloaded dataset location.

## Project Structure
```text
CNN_Flower_Classification/
├── dataset/
├── cnn_model.ipynb
├── trained_model.h5
├── requirements.txt
├── README.md
└── output_images/
    ├── accuracy_plot.png
    ├── loss_plot.png
    └── sample_prediction.png
```

## Conclusion
This project demonstrates how a CNN can classify flower images into five categories. The model learned useful image features, but the validation results indicate that further improvements are possible.
