# Genre Classification of Audio Files

This project aims to classify audio files into different genres using a Convolutional Neural Network (CNN) with TensorFlow and Keras. The dataset used is a collection of audio files in various genres. The model is trained and evaluated on this dataset, with performance metrics reported.

## Data Loading and Preprocessing

1. **Loading the Data**: The dataset is downloaded from Dropbox and extracted into the working directory. The dataset contains audio files in different genres.

2. **Audio Preprocessing**: The audio files are preprocessed to have a consistent sampling rate and length. The audio data is normalized and padded to a fixed length.

3. **Train-Test Split**: The dataset is split into training and testing sets. The training set contains 90% of the data, and the testing set contains 10% of the data.

4. **Data Serialization**: The preprocessed audio data and corresponding class labels are serialized and saved as pickle files for efficient loading during model training and evaluation.

## Model Architecture

1. **Conv1D Layers**: The model consists of multiple 1D convolutional layers with varying kernel sizes and strides. Each convolutional layer is followed by batch normalization, ReLU activation, and max pooling.

2. **Global Average Pooling**: A global average pooling layer is used to reduce the dimensionality of the feature maps.

3. **Dense Layer**: A dense layer with softmax activation is used for multi-class classification. The number of units in the dense layer corresponds to the number of genres.

## Model Training

The model is compiled with the Adam optimizer and categorical cross-entropy loss function. It is trained for 50 epochs with a batch size of 128. The learning rate is reduced on plateau to improve convergence.

## Training and Validation Accuracy

The model achieved a training accuracy of approximately 90% after 50 epochs. The validation accuracy was approximately 80% after 50 epochs.

## Performance Metrics

- **Precision**: The precision metric is used to evaluate the model's ability to correctly predict positive samples. The model achieved a precision of approximately 0.80.

- **Recall**: The recall metric is used to evaluate the model's ability to correctly identify all positive samples. The model achieved a recall of approximately 0.80.

- **F1-score**: The F1-score is the harmonic mean of precision and recall. The model achieved an F1-score of approximately 0.80.

- **Accuracy**: The accuracy metric is used to evaluate the overall correctness of the model's predictions. The model achieved a test accuracy of approximately 80%.

- **Loss**: The categorical cross-entropy loss is used to evaluate the model's performance during training and validation. The model achieved a test loss of approximately 0.40.
