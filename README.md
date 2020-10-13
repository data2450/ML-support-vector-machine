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

Larger values of C: less regularization(margin moderate ,small)

– Fit the training data as well as possible

– Each individual data point is important to classify correctly

Smaller values of C: more regularization(margin is  large)

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


