# Character Generation with Sherlock Holmes 🔍
Generate a semi-coherent English sentence using RNN architectures. Use of differing architectures (LSTM, GRU), layer structure (nodes and number of layers) and Window Size (100, 200, 300).

Download the saved models at this [link](https://drive.google.com/file/d/1Vvh3p1wEghT1_nc_OQz2uuoTVP1-STwd/view?usp=sharing).

## Recommended Hardware
* At least 16GB RAM
* An i7 Intel Processor (or equivalent)
* A NVIDIA GPU with 2GB VRAM (or equivalent)

## Software Packages
* [Anaconda🐍](https://www.anaconda.com/products/individual)
   * Tensorflow (which includes Keras) and Tensorflow-Base
   * Tensorflow GPU (optional)
   
```
conda install tensorflow
conda install tensorflow-gpu
```

## Processing Steps 
Place holmes.txt and Assignment_2_p2.ipynb in the same base directory (can be the same directory as used in [Part 1](https://github.com/RyanNgCT/RNNTasks/tree/master/Part%201))

## Results
| Model Number:  | Description/Type:                                           |Train Accuracy(%):|
| -------------  |:------------------------------------------------------------| ---------------- |
| 1              | LSTM RMSprop Base Win Size 100                              | 55.28            |
| 2              | LSTM RMSprop Add layer Win Size 100                         | 53.50            |
| 3              | LSTM Adam Base Win Size 100                                 | 54.28            |
| 4              | LSTM Adam Add layer, increase learning rate Win Size 100    | 46.13            |
| 5              | GRU RMSprop Base Win Size 100                               | 51.49            |
| 6              | GRU RMSprop add layer & dropout Win Size 100                | 43.88            |
| 7              | GRU Adam Win Size 100                                       | 51.17            |
| 8              | LSTM RMSprop Base Win Size 200                              | 55.91            |
| 9              | LSTM RMSprop Change learning rate, add dropout Win Size 200 | 38.60            |
| 10             | LSTM Adam Base Win Size 200                                 | 55.89            |
| 11             | LSTM Adam change learning rate Win Size 200                 | 15.83            |
| 12             | LSTM RMSprop change learning rate Win Size 200              | 56.76            |
| 13             | GRU RMSprop Base Win Size 200                               | 57.95            |
| 14             | GRU Adam Win Size 200                                       | 74.61            |
| 15             | LSTM RMSprop Win Size 300                                   | 54.09            |
| 16             | LSTM Adam Win Size 300                                      | 53.63            |
| 17             | GRU RMSprop Win Size 300                                    | 49.91            |
| 18             | GRU Adam Win Size 300                                       | 54.45            |

## Shortlist Evaluation
* Have a high final epoch training accuracy
* When I visual assess the words generated at last epoch for
  * Temperature = 0.5 and
  * Temperature = 1.0,
The model should have a high percentage of english words since the objective is to predict a semi-coherent sentence.

## Evaluation Criteria
*	Appropriate punctuations placements
*	Distributions of words and frequency of English words (check for repetition)
*	Be able to generate a label that can possibly be used construct and English word given a new input


Best Model: **Model 16** (see [report](https://github.com/RyanNgCT/RNNTasks/blob/master/DL_Assignment2_Report_NG%20CHIN%20TIONG%20RYAN.pdf) for scoring)

Sample of text generated:
```
--- Generating with seed: " he has notentirely lost his self-respect.your reasoning is certainly plausible.the further 
points, that he is middle-aged, that his hair isgrizzled, that it has been recently cut, and that he useslime-cream, 
are all to be gathered from a close examination of thelower part of the lining. the lens di"

------ temperature: 0.5
e stard of the stated at the country the stains and the door. it was a senter and that i had been the stains and seemed at 
the stains and that the stated with the side of the stard of the street. it was a star. it was a case of the street. 
it was a little which was a way and shall be a possible of the street. i asked, which i can be the case and before ip to 
any can to me the hat of the still man of the matter and succing at the letter of the street. it was not be bound to the 
drove which shall be somethat if thecound at the pation, and the could nate is a little not men and that he was something 
the great of the other uppasing and company which i have indicent for that i shall that there wa
```

