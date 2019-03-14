
## About use svm in nn
If using svm of sklearn in nn, there is no way to get the gradient from it. Use svm-loss instead.     
> As far as I know, SVM can only change its hyperplane without changing the input features. In other words，
it only assumes that its hyperplane is not perfect and would not think that the input was wrong.  
(https://discuss.pytorch.org/t/how-do-i-use-svm-in-nn/10686/4)
