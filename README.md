# NLP RNN vs LSTM Next-Word Prediction

**Name:** Noah C Frami  
**Date:** 11/20/2026

## Project Overview

For this project, I created two neural network models, a SimpleRNN and an LSTM, to predict the next word in a sentence. The goal was to train both models using the same text and compare their accuracy and predictions.

## How the Program Works

The program takes training text and converts the words into numbers using a tokenizer. It then creates groups of three words and trains the models to predict the next word.

Both models are trained for 150 epochs and tested using the same sentences.

## Project Files

- **main.py** - Contains the code for training and testing both models.
- **data.py** - Contains the training text.
- **requirements.txt** - Lists the required Python libraries.
- **README.md** - Explains the project and includes my reflection.

## Requirements

- Python
- TensorFlow
- NumPy
- PyCharm or another Python editor

## How to Run the Project

1. Download the project from GitHub.
2. Open the project folder in PyCharm.
3. Create or select a Python virtual environment.
4. Open the terminal and install the required libraries:

   `python -m pip install -r requirements.txt`

5. Run the program:

   `python main.py`

6. Wait for both models to finish training.
7. Review the accuracy scores and next-word predictions in the terminal.

## Model Comparison

**SimpleRNN:** This model processes words in order and uses information from previous words to make predictions.

**LSTM:** This model is designed to remember important information over longer sequences, which can help improve predictions.

Both models use an embedding layer, 32 hidden units, and a softmax output layer.

## Reflection Questions

### 1. Which model had better training accuracy?

I compared the training accuracy of both models after running the program. The model with the higher score performed better at learning the training data. This showed me how different neural network models can produce different results even when using the same text.

### 2. Which model gave more sensible next-word predictions?

I looked at the predicted words from both models and compared how well they fit the sentences. I learned that a model can have good training accuracy but still make predictions that do not always make sense.

### 3. Where did the SimpleRNN fail?

The SimpleRNN can struggle with remembering information from earlier words. This can cause it to make predictions that do not fit the sentence correctly. It also has limitations when working with longer sequences.

### 4. Why might the LSTM perform better on sequence tasks?

The LSTM is designed to remember important information for longer periods. This helps it understand patterns in sentences and can make it better at predicting words when more context is needed.

## Challenges

One challenge I had was getting TensorFlow to run correctly in PyCharm. Windows Smart App Control was blocking some of the TensorFlow files, which caused errors when starting the program.

I also had to fix an issue where the LSTM model was not being returned correctly, which prevented it from training.

After troubleshooting these problems, I was able to continue working on the project.

## Important Caution: Windows Smart App Control

During setup, Windows Smart App Control blocked a TensorFlow file called `pywrap_function_lib.pyd`.

The error message was:

`ImportError: DLL load failed: An Application Control policy has blocked this file.`

This is a Windows security restriction and does not necessarily mean there is something wrong with the Python code.

If this happens, check Windows Security and the Code Integrity logs to identify the blocked file.

**Caution:** Turning off Smart App Control reduces Windows security and generally cannot be reversed without resetting or reinstalling Windows. It is better to investigate the block before changing security settings.

## What I Learned

This project helped me understand how SimpleRNN and LSTM models work with text. I learned how tokenization, embedding layers, and training sequences are used for next-word prediction.

I also learned how to troubleshoot Python errors and TensorFlow installation problems.

## Conclusion

Overall, this project helped me better understand recurrent neural networks and how they can be used for natural language processing. Comparing the two models showed me how different approaches can affect prediction results.
