# what is support vector machine

Support Vector Machine (SVM) is a supervised machine learning algorithm capable of performing classification, regression and even outlier detection.
# working
The linear SVM classifier works by drawing a straight line between two classes. All the data points that fall on one side of the line will be labeled as one class and all the points that fall on the other side will be labeled as the second. Sounds simple enough, but there’s an infinite amount of lines to choose from. How do we know which line will do the best job of classifying the data? This is where the LSVM algorithm comes in to play. The LSVM algorithm will select a line that not only separates the two classes but stays as far away from the closest samples as possible. In fact, the “support vector” in “support vector machine” refers to two position vectors drawn from the origin to the points which dictate the decision boundary.
# linear classifier
A linear discriminative classifier would attempt to draw a straight line separating the two sets of data, and thereby create a model for classification
This is performed by fitting the liner equation to a sigmoid function.The out put will be +1 positive class and -1 negative class
we can see many lines that classify the datapoints.The best liner classifier is find out by ,the Linear classifier with maximum margin of classifier is called a  
Linear support vector machine(LSVM)

###classifier margin=defined as the maximum width the decision boundary area can be increased before hitting a data point

# regularisation
The strength of regularization is determined by C
(c controlls the margin between two classes)

Larger values of C: less regularization(fit the training set with few errors as possible,small immersion decision boundary)

– Fit the training data as well as possible

– Each individual data point is important to classify correctly

Smaller values of C: more regularization(tolernt to errors in favour capturaing the majority of datapoints correctly with a larger margin)

– More tolerant of errors on individual data points


# Pros:
• Simple and easy to train.
• Fast prediction.
• Scales well to very large
datasets.
• Works well with sparse data.
• Reasons for prediction are
relatively easy to interpret.

# Cons:
• For lower-dimensional data,
other models may have
superior generalization
performance.
• For classification, data may not
be linearly separable (more on
this in SVMs with non-linear
kernels)

# Model complexity
• alpha: weight given to the L1 or L2 regularization
term in regression models
– default = 1.0

• C: regularization weight for LinearSVC and
LogisticRegression classification models(default=1)

# non lineraly seprable svm
SVM, at its original form, can only classify linearly separable variables. Yet it can be easily adapted to conduct complex nonlinear classifications by adding non-linear features. A very powerful extension of linear support vector machines called kernelized support vector machine
# working of kernalized SVMS
they take the original input data space and transform it into new higher dimensional feature space,where it becomes much easier to classify the transform to data using a linear classifier.

# different kernals**
**1)Polynomial kernal**

Given a feature vector  [x1,x2,...,xn]  (bias not included), we can transform it to polynomial features, just like what we did in linear regression and logistic regression. For example, a 2nd degree polynomial transformation of  [x1,x2,x3]  through PolynomialFeatures(degree = 2, include_bias=False) will be  [x1,x2,x21,x22,x23,x1x2,x1x3,x2x3] . A SVM classifier can be trained on these new features. Instead of  w1x1+w2x2+w3x3+b , we will have  w1x1+w2x2+w3x21+w4x22+w5x23+w6x1x2+w7x1x3+w8x2x3+b . Let's look at the following example:

**2) RBF(radial basis function kernal)

Another way to construct non-linear SVM is to add new features by computing the similarity between each datapoint  x   to certain landmarks  l . A popular definition of the similarity function is the Gaussian Radial Basis Function (RBF):

ϕγ(x,l )=exp(−γ∥x − l∥^2)
Where  ∥x⃗ −l⃗ ∥2=(x1−l1)2+(x2−l2)2+...+(xn−ln)2 . In case of a 1D input feature  x  and a landmark  l=0 , we can plot the similarity function as follows:

