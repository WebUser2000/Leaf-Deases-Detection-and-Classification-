This project focuses on the detection and classification of plant leaf diseases using Deep Learning and Convolutional Neural Networks (CNN). The objective of the project is to help in the early identification of crop diseases through image-based analysis so that farmers and agricultural researchers can take preventive measures at the right time.

The model analyzes leaf images and predicts whether the plant is healthy or affected by a specific disease. The project was implemented using Python, TensorFlow, and Keras in Google Colab.

Features
Image-based plant disease detection
Deep Learning based CNN model
Multi-class disease classification
Training and validation accuracy visualization
Data preprocessing and augmentation
Real-time prediction support for leaf images
Technologies Used
Python
TensorFlow
Keras
NumPy
Matplotlib
OpenCV
Google Colab / Jupyter Notebook
Dataset

The dataset contains images of healthy and diseased plant leaves collected from:

Public agricultural datasets
Online repositories
Field observations and sample images
Disease Classes

Some of the disease categories used in the project include:

Tomato Healthy
Tomato Late Blight
Potato Early Blight
Pepper Bacterial Spot
Project Structure
Plant-Leaf-Disease-Detection/
│
├── dataset/
│   ├── train/
│   ├── validation/
│   └── test/
│
├── models/
│   └── cnn_model.h5
│
├── notebooks/
│   └── Plant_Disease_Detection.ipynb
│
├── outputs/
│   ├── accuracy_graph.png
│   ├── loss_graph.png
│   └── predictions/
│
├── README.md
└── requirements.txt
Deep Learning Model

The project uses a Convolutional Neural Network (CNN) architecture for feature extraction and disease classification.

Model Architecture
Rescaling Layer
Convolutional Layers
MaxPooling Layers
Dropout Layers
Flatten Layer
Dense Layers
Softmax Output Layer
Installation

Clone the repository:

git clone https://github.com/your-username/Plant-Leaf-Disease-Detection.git

Move into the project directory:

cd Plant-Leaf-Disease-Detection

Install required dependencies:

pip install -r requirements.txt
Training the Model

Run the notebook or Python script to train the CNN model:

python train.py

or open the Jupyter Notebook:

jupyter notebook
Sample CNN Code
from tensorflow.keras import layers, models

model = models.Sequential([

    layers.Rescaling(1./255, input_shape=(128,128,3)),

    layers.Conv2D(32, 3, activation='relu'),
    layers.MaxPooling2D(),

    layers.Conv2D(64, 3, activation='relu'),
    layers.MaxPooling2D(),

    layers.Conv2D(128, 3, activation='relu'),
    layers.MaxPooling2D(),

    layers.Dropout(0.2),

    layers.Flatten(),

    layers.Dense(128, activation='relu'),

    layers.Dropout(0.2),

    layers.Dense(num_classes, activation='softmax')
])
Results

The model achieved good performance during training and testing.

Observed Performance
Training Accuracy: ~90–95%
Validation Accuracy: ~88–93%
Testing Accuracy: ~90%

The model successfully classified healthy and diseased leaves with satisfactory accuracy.

Challenges Faced

During implementation several practical issues were observed:

Large dataset memory usage
Google Colab RAM crashes
Similar appearance between diseases
Lighting variation in images
Overfitting during training
Solutions Implemented
Reduced image size
Used dropout layers
Applied data augmentation
Reduced batch size
Used dataset prefetching
Future Improvements
Mobile application integration
Real-time camera disease detection
Cloud deployment
Support for more crop diseases
IoT based smart agriculture integration
Applications
Smart Agriculture
Crop Monitoring
Automated Disease Detection
Agricultural Research
Farmer Assistance Systems
Conclusion

This project demonstrates the application of Deep Learning in agriculture for automated plant disease detection. The CNN-based model can identify disease patterns from plant leaf images and can assist in early diagnosis and crop protection.

Author

 Kumar Sahil 
Integrated B.Tech + M.Tech
Central University of Jharkhand

License

This project is developed for academic and research purposes.
