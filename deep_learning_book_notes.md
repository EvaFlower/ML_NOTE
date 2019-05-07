
## Chapter 5 Machine Learning Basics  
5.1 various tasks in machine learning; 0-1 loss on classification to measure accuracy of the model; average log-probability  
 of the model assigning to the samples on density estimation; mean square loss on the linear regression
 
5.2 Capacity of model; underfitting and overfitting; Occam's razor -- simple working model is better; VC dimension; no free   
lunch theorem; regularization
  
5.3 training data -- training set (80%) and validation set (20%); testing data -- test set; k-fold cross-validation for small  
dataset
  
5.4 bias of an estimator: unbiased estimator; variance of an estimator: biased estimate of the true standard deviation of  
data, use square root of the unbiased estimator of the variance, can calculate the like 95% confidence interval centered on  
the estimator, compare A and B algorithm  
  
5.5 maximum likelihood estimation: any loss consisting of a negative log-likelihood is a cross-entropy between the empirical distribution defined by the training set and the probability distribution defined by model; linear regression can be viewed 
as maximum likelihood with the assumption of gaussian model; regularization strategies such as weight decay can be used to 
obtain a biased version of maximum likelihood that has less variance when training data is limited.
