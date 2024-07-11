# Facial-Emotion-Recognition
## Introduction
Facial expression recognition (FER) technology revolutionizes customer behavior analysis by identifying emotional responses from facial cues. Businesses can gain insights into customer satisfaction, preferences, and engagement, enhancing marketing strategies, customer service, and personalized shopping experiences.

## Data Presentation and Preparation
### Dataset: 
48x48 pixel grayscale images of faces categorized into seven emotions (Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral).
### Training Set: 
28,709 examples.
### Test Set:
3,589 examples.
### Steps:
Read and display images.
Define the directory and classes.
Display one image per class.
Resize images to 224x224 pixels.
## Deep Learning
### Data Preparation:
Load and preprocess images.
Shuffle and extract features and labels.
Normalize pixel values to the [0, 1] range.
Split data into training (80%) and testing (20%) sets.
### MobileNetV2 Model Implementation:

#### Architecture:
Optimized for mobile devices with inverted residual blocks and depth-wise separable convolutions.
#### Key Features:
##### Inverted Residual Blocks: 
Efficient parameter use and gradient flow.
##### Depth-wise Separable Convolutions: 
Reduced computational cost.
##### GlobalAveragePooling2D and Dense Layers:
For feature aggregation and classification.
#### Implementation:
Load pre-trained MobileNetV2 without the top layer.
Freeze base model layers.
Add custom layers for FER.
Compile and train the model using ImageDataGenerator for data augmentation.
Fine-tuning by unfreezing some base model layers and applying advanced data augmentation techniques.
#### Modes:

##### Simple Mode:
Load MobileNetV2, add custom layers, compile, and train for 25 epochs.
##### Advanced Mode:
Apply data augmentation, fine-tune the model by unfreezing layers, compile, and train for 25 epochs.
#### Model Evaluation and Saving
Evaluate the model's performance on the validation set during training.
Save the trained model for future use.
### EfficientNetB0 Model Implementation
#### Data Preparation:
Similar to the steps used for MobileNetV2.
#### Architecture:
Optimized for both accuracy and efficiency using compound scaling.
#### Key Features:
##### Compound Scaling: Balances network depth, width, and resolution.
##### Swish Activation Function: Improves model performance.
#### Implementation:
Load pre-trained EfficientNetB0 without the top layer.
Freeze base model layers.
Add custom layers for FER.
Compile and train the model using ImageDataGenerator for data augmentation.
Fine-tuning by unfreezing some base model layers and applying advanced data augmentation techniques.
