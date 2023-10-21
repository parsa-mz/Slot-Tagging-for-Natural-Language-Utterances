## Slot Tagging for Natural Language Utterances


## Introduction

The goal of this project is to train a model to tag slots in natural language utterances of users addressing a virtual personal assistant. 


## Requirements

The project uses [Python 3.10](https://www.python.org/downloads) which has some linting defaults which may cause import
errors if using python < 3.10 and [PyTorch](https://pytorch.org/)

The requirements can be installed using the following command:

```bash
    # create a virtual environment
    py -m venv env
    # windows only
    env\Scripts\activate
    # linux or mac
    source env/bin/activate
    
    # install requirements
    pip install -r requirements.txt
```

Alsp you should download glove embeddings from [here](https://www.kaggle.com/datasets/rtatman/glove-global-vectors-for-word-representation/download?datasetVersionNumber=1) and put them in the `data` folder. The zip file contains 3 files, we only use the `glove.6B.100d.txt` file. 

If the file is too big, you can use the `glove.6B.50d.txt` file instead. After that you should change the `input_dim` (`embedding size`) to 50.


## Running the code

The code has been written in jupyter notebook so that each part can be run individually and test different senarios and variables along the way. The notebook can also be imported into colab as well if you prefer working in the cloud GPU.



## Project Structure

The project is structured as follows:

```bash
    .
    ├── data
    │   ├── hw1_test-2.csv
    │   ├── hw1_train-2.csv
    │   └── sampleSubmission-2.csv
    ├── output
    │   ├── best_model.pt
    │   └── submission_labels.csv
    ├── README.md
    ├── requirements.txt
    └── notebook.ipynb
```

The `data` folder contains the data files for the project. The `notebook` is a jupyter notebook which contains the code
for the project. 


## Model

For this assignment, I've used different models with different structres, including bi-LSTM, MLP, with different number of hidden layers and methods like dropout, different learning rate, and using leaky relu activation. 



## Authors

Parsa Mazaheri, Dec 2022