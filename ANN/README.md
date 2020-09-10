# Artificial Neural Network

I will share the important theory/basics behind ANN and following that will go and implement those from scratch in Pytorch

Before going to what neural network is , let's take a small step understand what a single computation unit is? and will extrapolate those to form a deep neural network. 

## Perceptron Model

Let's take simple computation y = x1+x2

 ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/ANN1.png)  
 
Here there is no way for function to adjust itself to learn to produced the defined output y, there should be some factor added to the input which can be adjusted. 
Let's mulitply an adjuatable factor named weights w1 and w2. so that w1 and w2 will be learned and adjusted to produce a desired output y.
I mean each time w1, w2 gets updated to effect y.

 ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/ANN2.png)  
 
 But what happens if input x1 is 0, then whatever update w1 has, will not have any impact on y.To avoid this situation, the bias b1, b2 is added for simplification. 
 
  ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/ANN3.png)  
  
 In the real world it not just restricted to just 2 inputs and it goes to the n levels and hence the generalization below
 
  ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/ANN4.png)  
  
  
  Generalizing the above outcome into one formula unit as below
  
   ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/ANN5.JPG)  
   
   The single perceptron model will not suffice to learn complicated systems. Let's expand the signle perceptron model to multi-layer perceptron model.
   
   ## Multi layer perceptron Model
   
  We build layer of perceptron like below, the output of one perceptron is fed into as input to another perceptron. 
  The first layer is called input layer and this is the layer which receives the data and last layer is output layer and it is closely associated with the label we predict, any layer in between is called hidden layer. 
  If the network has 2 or more hidden layer then it is considered as deep neural network. The neural network can approximate any function and it outbeats all other traditional machine learning accuracy.
  
   ![alt text](https://github.com/barathvaj/NLP-Learning-And-Training/blob/master/Images/ANN6.png)  
   
   ## Activation Functions
   
  contnd...
  
  
  
  
  
 
 
