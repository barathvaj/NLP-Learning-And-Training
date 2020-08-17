# Installation
## Anaconda 

[Windows](https://docs.anaconda.com/anaconda/install/windows/)   
[Mac](https://docs.anaconda.com/anaconda/install/mac-os/)    
[Linux](https://docs.anaconda.com/anaconda/install/linux/)   

### Use the Anaconda Prompt to install prerequisites for NLP Learning Environment
```bash
cd <SourcePath>
conda env create -f environment.yml
conda activate nlplearnenv
jupyter notebook
```

# Numpy - Numerical Processing Library handles large datasets stored as arrays effeciently

- [Numpy Basics](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Installation%20and%20Basics/Numpy%20Basics.ipynb) - Arrays, Slicing, Indexing, Operations
- [Numpy Exercises](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Installation%20and%20Basics/Numpy-Exercises.ipynb) - To familize by practicing the concept learnt
- [Numpy Exercises With Solution](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Installation%20and%20Basics/Numpy-Exercises%20-%20With%20Solutions.ipynb) - To review the practised solution with the Problems

# Pandas - Data manupulation and analysis.
- [Pandas Basics](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Installation%20and%20Basics/Pandas%20Basics.ipynb) - To exercise all the basics functions and concepts of pandas

# PyTorch Tensors and Operation
- [Pytorch Basics](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Installation%20and%20Basics/Pytorch%20Basics%20Exercises.ipynb) - To familize by practicing the concept learnt
- [Pytorch Basics With Solutions](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Installation%20and%20Basics/Pytorch%20Basics%20Exercises%20-%20With%20Solutions.ipynb) - To familize by practicing the concept learnt
- [Pytorch Cuda - Basics](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Installation%20and%20Basics/Pytorch-Cuda.ipynb) - Basic Operations of tensor with CUDA
# Machine Learning Basics

In my words, automated way to find hidden patterns from historical data and with that it arrives decisions for the present or future. Since we are much focused in text processing here, let see some examples related to that scenario

Examples - Text Classification, Topic modeling, Text Sentiment analysis, Entity extraction, Machine translation.- Will try to go into detail of the same in upcoming learnings

Two Types

1) Supervised Learning
   -- Labeled Data - Means for each set of input we already knows the desired outcome is
   
   For Example - Text classification by topic, Postive vs negative movie review
   
   Machine Learning Process
   
   1) Data collection
      -  Include only the data which contributes to model outcome       
   2) Data Preparation
      -  Cleaning data(removing duplicates, augmentation, deal with missing values, data normalization)
      -  visualize data and class imbalances
      -  Data split - Train, Validataion and Test Set
   3) Select a Algorithm
      -  With some exploration i am biased towards a neural network here(experiment with pretrained/custom models), and any decision tree algorithm. The neutral networks which simply outbeats the traditional machine learning alogrithms.
   4)  Model Training
       - It is iterative process, each iteration it try to adjust it weights to maximize the prediction
   5) Model Evaluation
       - At each iteration, model get evalauted in both training and validation set. The ultimate goal is to reach maximum accuracy by balancing it between training and validation set. I mean prevent underfitting vs overfitting. 
       - How we evaluate the model perfromance it differs between classification and regression. 
   6) Model Tuning
       - Tune the model parameters to increase it parameters. 
       - For example: Changing learning rate or having different learning rate for each layer group, adding a regularization factor etc.
    7) Model Prediction
       - Evaluate model with test set , approximation in real world. 
     
     
  ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/ML_process.png) 
  
## Overfitting vs Underfitting
  
   ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/overfit.png) 
  
  Overfitting
  -   Model fits too much with the training set, it leads to low error in training set and high errors in validation/test sets. It is because model not able to genralize instead it memorizes the data.
  -   One way to fix here is to use to reduce the input data(reduced features etc,) and increase regularization factor.
  -   Increase in error in test set and error in training set still going down, a better point to stop the training process
  
  Underfitting
  -   Model not captured the enough patterns from training set results in high training error. 
  -   Collect more samples, data augementation, increased iteration helps in fix the same
  
