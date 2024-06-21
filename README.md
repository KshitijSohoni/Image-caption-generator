# Image caption generator
###This project focuses on generating captions for images using deep learning techniques. The dataset used is the Flickr8k dataset, which contains 8000 images each paired with five different captions. The model is trained to map image features to captions using a combination of Convolutional Neural Networks (CNNs) and Long Short-Term Memory networks (LSTMs).


### Libraries Used
- numpy
- pandas
- tensorflow
- keras
- tqdm
- pickle

### Feature Extraction
We use the VGG16 model pre-trained on ImageNet to extract features from the images. The fully connected layers are removed, and the output is taken from the last convolutional block.

## Model Architecture
The model architecture consists of:

**Encoder**: A CNN (VGG16) to extract image features.
**Decoder**: An LSTM network to generate sequences (captions) from the encoded image features.

### Training
**Data Generator**: A custom data generator is used to handle large datasets and avoid memory issues.
**Model Training**: The model is trained using the Adam optimizer and categorical cross-entropy loss.

The model is evaluated based on its ability to generate accurate and descriptive captions for the images. The performance can be measured using BLEU scores or manual evaluation of the generated captions.

### BLEU-1 score: 0.390204
### BLEU-2 score: 0.190610
