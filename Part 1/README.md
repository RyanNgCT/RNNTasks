# Sentiment Analysis with Em😂ticons 

Mapping labelled sentiments to emoticons...

😍  *In Love*
😂  *Tears of Joy*
📷  *Camera*
🔥  *Flames*
❤  *Black Heart* (supposed to be rendered in black)

## Recommended Hardware
* At least 16GB RAM
* An i7 Intel Processor (or equivalent)
* A NVIDIA GPU with 2GB VRAM (or equivalent)

## Software Packages
* [Anaconda 🐍](https://www.anaconda.com/products/individual)
   * Tensorflow (which includes Keras) and Tensorflow-Base
   * Tensorflow GPU (optional)
   
```
conda install tensorflow
conda install tensorflow-gpu
```

## Processing Steps & Data Sampling
1. Firstly, place dataset.csv (which contains the tweets and the corresponding sentiment labels from 0 to 4) and mapping.csv (which contains the labels and the corresponding emoticons), as well as the Assignment_2_p1.ipynb must be placed in the **same base directory**.
```
DL Assignment 2
|- dataset.csv
|- mapping.csv
|- Assignment_2_p1.ipynb
```

2. Pick a random state. Replace `?` with an integer. This ensures that all the models get trained on the same training data and assessed by the same testing data. In my case I was assigned `40`.
```
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state = ?)
```

## Results
| Model Number:  | Description/Type:                                      |Test Accuracy (%):|
| -------------  |:------------------------------------------------------ | ---------------- |
| 1              | Non-PT LSTM RMSProp Base                               | 62.75            |
| 2              | NonPT LSTM RMSprop Add 1 layer                         | 62.59            |
| 3              | NonPT LSTM RMSprop Add L2 reg; change batch size       | 62.54            |
| 4              | NonPT LSTM Adam Base                                   | 63.36            |
| 5              | NonPT LSTM Adam Add L2 reg                             | 62.94            |
| 6              | NonPT LSTM Adam 1 layer; increase batch size           | 63.41            |
| 7              | NonPT GRU RMSprop Base                                 | 62.44            |
| 8              | NonPT GRU RMSprop add dropout                          | 62.56            |
| 9              | NonPT GRU RMSprop increase dropout; change batch size  | 61.77            |
| 10             | NonPT GRU RMSprop increase nodes                       | 62.88            |
| 11             | NonPT GRU Adam Base                                    | 63.03            |
| 12             | NonPT GRU Adam increase dropout                        | 62.29            |
| 13             | PT LSTM RMSprop Base glove50*                          | 54.71            |
| 14             | PT LSTM RMSprop glove50 FT1*                           | 54.79            |
| 15             | PT LSTM RMSprop glove100 FT2                           | 63.09            |
| 16             | PT LSTM RMSprop glove200 FT3                           | 63.43            |
| 17             | PT LSTM Adam glove100 Base                             | 62.74            |
| 18             | PT LSTM Adam glove200 add reg and dropout              | 63.63            |
| 19             | PT LSTM Adam glove200 FT1                              | 62.02            |
| 20             | PT GRU Adam glove100 Base*                             | 55.98            |
| 21             | PT GRU Adam glove200 FT1                               | 64.37            |
| 22             | PT GRU RMSprop glove100 Base                           | 62.78            |
| 23             | PT GRU RMSprop glove100 FT1                            | 63.16            |
| 24             | PT GRU Adam glove200 FT2                               | 64.54            |
| 25             | PT GRU Adam glove200 FT3                               | 64.69            |

*pretrained models without unfreezing layers for backpropagation

## Best Model Evaluation
* Not overfit too quickly
*	Have good accuracy of above 62% (which is the average of the models)
*	Be able to correctly predict most of the corresponding emoticons based on the sentiment supplied

Best Model: **Model 25** (see [report](https://github.com/RyanNgCT/RNNTasks/blob/master/DL_Assignment2_Report_NG%20CHIN%20TIONG%20RYAN.pdf) for scoring)


