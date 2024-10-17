
# Text Generation Using LSTM

## 1. Introduction

This project involves text generation using a Long Short-Term Memory (LSTM) neural network model. The objective is to predict science fiction (scifi) text based on a given corpus. The project uses a deep learning model to learn patterns from the input data and generate novel sequences of text.

## 2. Objective

The main objective of this project is to build a model capable of generating scifi text using LSTM networks.

## 3. Project Structure

- **Notebook**: Contains the code for training, evaluating, and generating text using the LSTM model.
- **Pre-trained Model**: A trained model is included for quick evaluation without re-running the entire training process.
- **Data File**: The scifi text corpus is provided separately and needs to be placed in the specified directory.

## 4. Data Processing

1. **Text Cleaning**: The input text is cleaned by removing punctuations and special characters.
2. **Corpus Preparation**: 
   - The text is split into individual words and stored in a list (`text_corpus`).
   - A dictionary of unique words is created.
   - The list of words is converted into sequences where each sequence contains 31 words (30 input words followed by 1 target word).
3. **Tokenization**: The word sequences are tokenized and converted into NumPy arrays for input into the model.

## 5. Model Architecture

The model uses an LSTM network with the following structure:
- **Embedding Layer**: For tokenized word input.
- **Two LSTM Layers**: Each with 64 units.
- **Dense Layer**: 128 nodes.
- **Output Layer**: Predicts the next word in the sequence.

### Hyperparameters:
- **Optimizer**: Adam optimizer with a learning rate of 0.001.
- **Activation Function**: ReLU.
- **Loss Function**: `sparse_categorical_crossentropy` to avoid memory issues with one-hot encoding.
- **Batch Size**: 32.

## 6. Steps to Run the Project

1. **Download the project**: 
   - Unzip the folder and place the text file (`internet_archive_scifi_v3.txt`) in your drive at the following path:  
     `/content/drive/MyDrive/language_model/internet_archive_scifi_v3.txt`
   
2. **Run the Notebook**: 
   - To train the model, follow the cells under the "Model Training" section.
   - If you want to skip training and directly use the pre-trained model, load it and execute the "Model Evaluation" section.

3. **Important**:
   - Ensure you have sufficient computational power, as training time can vary depending on your system.
   - On non-Windows OS, you may need to adjust the encoding.

## 7. Example Results

### Input:

```plaintext
He moved slowly and with a kind of painful dignity, as a man moves on his way to the firing squad. A rumpled shock of black hair pointed up the extreme pallor of a gaunt face.
```

### Output:

```plaintext
He moved forward through the darkness, feeling the weight of the unknown pressing on him. His thoughts drifted to the stars above, wondering if they held the answers he sought. The silence around him was deafening, but in it, he found a strange comfort, as if the universe itself was guiding his steps.
```

## 8. Report

A detailed report of the project is available in the report submitted on NESS.

## 9. Dependencies

The following Python libraries are required:
- `NumPy`
- `TensorFlow`
- `Keras`
- `nltk`

You can install them using the following command:

```bash
pip install numpy tensorflow keras nltk
```

## 10. Conclusion

This project demonstrates the use of an LSTM model for generating scifi text. The model successfully learns patterns from the input corpus and can generate new sequences that resemble meaningful and coherent scifi narratives, though improvements can be made through further tuning.
