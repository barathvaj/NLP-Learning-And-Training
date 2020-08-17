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

## Supervised Learning
   Labeled Data - Means for each set of input we already knows the desired outcome is
   
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
  
### Overfitting vs Underfitting
  
   ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/overfit.png) 
  
  Overfitting
  -   Model fits too much with the training set, it leads to low error in training set and high errors in validation/test sets. It is because model not able to genralize instead it memorizes the data.
  -   One way to fix here is to use to reduce the input data(reduced features etc,) and increase regularization factor.
  -   Increase in error in test set and error in training set still going down, a better point to stop the training process
  
  Underfitting
  -   Model not captured the enough patterns from training set results in high training error. 
  -   Collect more samples, data augementation, increased iteration helps in fix the same
  
 ### Evaluation Metrics 
 Let's dig little deeper into the evaluation metrics, let's try to apply the right metrics for 2 common problems Classification(classify a label/category for given input data) and  Regression(predicting the future continuos values). 
 
 #### Classifcation Metrics
There are 4 common ways to measure the classification metrics. Let's take an example, and describe the example with different metrics. 

##### Movie review - Classify whether the review is postive or negative. 
The example is simple binary classification. 

###### Accuracy
Say we got 100 reviews for moview , out of 100 it able to predict right for 90 of the reviews by saying postive or negative. It means it is 90% accurate. 
- Accuracy = number of right predictions/Total number of predictions

The problem here it works well with the balanced set, i mean if you get 80 postive reviews and 20 negative reviews. It able to predict all positve reviews and none of negative reviews yields 80% accuracy. It is not suited for the unbalanced set scenario like above.  

###### Confusion Matrix (Precision vs Recall)
   ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/conmatrix.jpg) 
   
   There are 4 important metrics below, it helps to arrive with the precision and recall metrics
   True Positive(TP) - Model correctly predicts the positive class
   True Negative(TN) - Model correctly predicts the negative class
   False Positive(FP) - Model incorrectly predicts the positive class
   False Negative(FN) - Model incorrectly predicts the negative class
   
Recall 
- What proportion of actual positives was identified correctly - TP/TP+FN
- It punishes the model which has false negative. I mean model without false negative will have high score.

Precision 
- What proportion of positive identifications was actually correct - TP/TP+FP 
- It means it punishes the data with false positives. I mean model without false posives will have high score.

F1 Score
-  Genarally in realtime we tradeoff between the Precision and Recall. To get the balance between the both, we combine bith precision and recall metrics
-  Formulated by 2*(precision*recall)/(precision+recall)
-  It punishes the extreme difference between precision and recall, say for ex: your recall is 1.0 and precision is 0.0. it you just take a simple average it gives you 0.5, but f1 score gives you the value 0. 

It all depends on the situation, which takes a lead or usage of F! score is optimal. For example let's take a example of diagnosing whether patient has cancer or not. I will prefer taking precision over recall here because identiying the patient with cancer as not an cancer is more severe than identifying the patient with no cancer as cancer. 
Generally in this case we will have addition step performed by medical expert to confirm the state. 

 #### Regression Metrics
 Model which used to predict continuous values like for example predicting the sales price, property value. 
 
 ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/regmatrix.JPG)  
 
 ##### Mean Absolute Error
 - Absolute value of average of differences between Actual value and predictions. 
 - The problem here , it not punishes the large differences. 
 
 ##### Mean Squared Error
 - Here larger error will be more punished, since we taking square of difference here
 - It is nothing but a Square of average of differences between Actual value and predictions
 - difficult to intepret , since it is different metrics as y, since it gives equal to y square.
 
 ##### Root Mean Squared Error
 - It is root of Mean squared error, it punishes the large difference also it also equates to the same unit as y. 
 
## UnSupervised Learning

When we don't have labels/outcomes and it falls under unsupervised learning. 

### Clustering
-  Grouping the similar data points together which helps identify different categories with in the dataset.

### Dimension Reduction
Reduces number of features in dataset either for compression or proper visualization of trends in historical data

